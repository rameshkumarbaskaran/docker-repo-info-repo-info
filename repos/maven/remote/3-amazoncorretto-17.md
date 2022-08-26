## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:ec9d031a0ad31ebd406a45b5c0b8c82f7ba915712158e53c8906249c61620e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:0ebf2ced4148145a24c53ce8e7a09782a25b56113fa48615dc7301b135d725b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226358978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884a23a3f6f486008d772a67d99cc3ba2a44345ef3040c4eb1df7698065911ee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 26 Aug 2022 01:19:36 GMT
ADD file:ebfd33425a17b16a9e560de15c91108bf2ee740f284a1482a7105b420ff22678 in / 
# Fri, 26 Aug 2022 01:19:37 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 02:04:12 GMT
ARG version=17.0.4.9-1
# Fri, 26 Aug 2022 02:04:48 GMT
# ARGS: version=17.0.4.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 02:04:48 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 02:04:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 26 Aug 2022 02:25:56 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 26 Aug 2022 02:25:56 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 26 Aug 2022 02:25:56 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Aug 2022 02:25:56 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 26 Aug 2022 02:25:56 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 26 Aug 2022 02:26:02 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 26 Aug 2022 02:26:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Aug 2022 02:26:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Aug 2022 02:26:02 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 26 Aug 2022 02:26:02 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 26 Aug 2022 02:26:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Aug 2022 02:26:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd06b60db4951fd95b43a9e73fb084fe7d2afcd4ff464472ead5548cd1c28717`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 62.3 MB (62326701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb036d0e9663b7f913ccd85668091b61213d2f809739041c219aa4150e95baf8`  
		Last Modified: Fri, 26 Aug 2022 02:08:22 GMT  
		Size: 151.7 MB (151663675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b755cda3341d0a9d25bf02f286b591c99cbfa558496501f82092e4a8d9c5a5`  
		Last Modified: Fri, 26 Aug 2022 02:30:16 GMT  
		Size: 3.6 MB (3627878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be1a5741775b702645d6ba798ae469b5fd601007d298fc1b6abd462a68b6422`  
		Last Modified: Fri, 26 Aug 2022 02:30:17 GMT  
		Size: 8.7 MB (8739511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7512a29b43153278b0f7ddaedd16dfc7c12d9c8d9e8855739d87da621a14188`  
		Last Modified: Fri, 26 Aug 2022 02:30:16 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a00484c3c57b2f543e1b733bc47fb0feac0bf696f6759e98571108d259885`  
		Last Modified: Fri, 26 Aug 2022 02:30:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c80eeda42dcc01727d53adfc7e31dbbb4ff904f40fa89fa9a8f816c4a5bf1853
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226505348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1687a32af3cf16fbeccea237062a347aeacf0d3d8b191466a82745356d591bb9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:01:47 GMT
ARG version=17.0.4.9-1
# Fri, 26 Aug 2022 01:02:06 GMT
# ARGS: version=17.0.4.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:02:06 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:02:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 26 Aug 2022 01:23:01 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 26 Aug 2022 01:23:02 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 26 Aug 2022 01:23:03 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Aug 2022 01:23:04 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 26 Aug 2022 01:23:05 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 26 Aug 2022 01:23:15 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 26 Aug 2022 01:23:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Aug 2022 01:23:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Aug 2022 01:23:19 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 26 Aug 2022 01:23:20 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 26 Aug 2022 01:23:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Aug 2022 01:23:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d9f6ed17988abb0810c79c739409f7131a60308790d99bb799d5cf30aa148a`  
		Last Modified: Fri, 26 Aug 2022 01:04:43 GMT  
		Size: 150.2 MB (150177681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234e11cb34b00ef37d7b31f14149e07ef68505e88670e673b9e38d3955f2210`  
		Last Modified: Fri, 26 Aug 2022 01:27:51 GMT  
		Size: 3.6 MB (3648203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d19db9093f86f8e6b3a303ff6aa5e80418d35e0af13a77f3442dd1d1ac16e8`  
		Last Modified: Fri, 26 Aug 2022 01:27:52 GMT  
		Size: 8.7 MB (8739484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627a2f9e78bff1de0202bf9ed73a4998938346c23286909bb1e76b5516121b7d`  
		Last Modified: Fri, 26 Aug 2022 01:27:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e5eea44a0abb6518afe33bfd39c16b71adf7c6adf9cb4062ef416f0d82a171`  
		Last Modified: Fri, 26 Aug 2022 01:27:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
