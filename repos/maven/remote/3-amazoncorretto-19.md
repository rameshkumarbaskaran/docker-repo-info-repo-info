## `maven:3-amazoncorretto-19`

```console
$ docker pull maven@sha256:ee5cbc4ec3efb5462ee694236144f84c94ddd574e27da43995a3e6d0cfba52af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-19` - linux; amd64

```console
$ docker pull maven@sha256:e669b2ed863d952c0473bf3d0ba522733846e2448d6bfc5d30fb27191af1a153
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234047580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d0606e36bff1daad2a5c24f4feaeba668e7f6d61d553cf13311e8381c414ab`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:52:00 GMT
ARG version=19.0.1.10-1
# Thu, 17 Nov 2022 01:52:24 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:52:25 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:52:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Thu, 17 Nov 2022 02:32:58 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:32:58 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:32:58 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:32:58 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:32:58 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:33:04 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:33:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:33:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:33:05 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:33:05 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:33:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:33:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3688498541e6d412d3fb40c195df25ef434028c0c3e0fe022966c47fede444f4`  
		Last Modified: Thu, 17 Nov 2022 01:56:46 GMT  
		Size: 159.4 MB (159399711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf0f8e90224d347a1840704ae52808e064b95f352bd28f3d07b3076fda0e8d1`  
		Last Modified: Thu, 17 Nov 2022 02:35:59 GMT  
		Size: 3.6 MB (3644931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac39ae4739f7f1b1939373258df35f522ed94a770ff9b1f8da7c1823f0bcdfb2`  
		Last Modified: Thu, 17 Nov 2022 02:35:59 GMT  
		Size: 8.7 MB (8739500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02f4e0293825cd2e0684399cb6843163dba0058c3ddce841f99b99a756e7577`  
		Last Modified: Thu, 17 Nov 2022 02:35:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78f79aa9bb4954ce5ca19f5ddbd08b203f56f39759a99024aba2dee6a38e39c`  
		Last Modified: Thu, 17 Nov 2022 02:35:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-19` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6e053123a655c4e85ee42b3c848e2eb42c3be3f1584d6ab3dd079edd8b9e48b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234183858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7cb3cefefe4d4aa9bd70b709e9e8e1af3f9294e6fb30731002769acfd519b2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:01:40 GMT
ARG version=19.0.1.10-1
# Fri, 16 Dec 2022 01:01:59 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 01:02:01 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:02:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Fri, 16 Dec 2022 01:22:52 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 16 Dec 2022 01:22:52 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 16 Dec 2022 01:22:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Dec 2022 01:22:52 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 16 Dec 2022 01:22:52 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 16 Dec 2022 01:22:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 16 Dec 2022 01:22:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Dec 2022 01:22:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Dec 2022 01:22:54 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 16 Dec 2022 01:22:54 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 16 Dec 2022 01:22:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Dec 2022 01:22:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a522d703ce658eafb2884db6606c458357c76578aa4a908df5bfdeab0f214a97`  
		Last Modified: Fri, 16 Dec 2022 01:06:12 GMT  
		Size: 157.8 MB (157832709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e542c6b0d8f59679f781e6ee666378e6eb4dd770aa2529d2157146c8917d7cca`  
		Last Modified: Fri, 16 Dec 2022 01:25:10 GMT  
		Size: 3.6 MB (3646238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865fc40591474c23db75486cfe00f6e8d101b99d7bedb2c8f473727afe408e0a`  
		Last Modified: Fri, 16 Dec 2022 01:25:10 GMT  
		Size: 8.7 MB (8739487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3419cf13d5c712d6e23821e3e025a3859bde377248d34e6a1e82af530d12b`  
		Last Modified: Fri, 16 Dec 2022 01:25:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8694a136df2a06c1c7547058086e4d4ce4ac7303fc45b1ff874a59958f2b37c5`  
		Last Modified: Fri, 16 Dec 2022 01:25:09 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
