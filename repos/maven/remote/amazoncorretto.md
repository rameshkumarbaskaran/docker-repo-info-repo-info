## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:ab45677650fce6f67ff6eb957005ce02cc280b314f4d88e292e83c7c325bb346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:3204b8dae96d8075eb697b99be21e8559da001da4c0aac098e2b83d71567d760
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222413660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf979acd797a18e06c420f50d439b225fe1d205473e7b63900bd1b31b7af0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:50:32 GMT
ARG version=11.0.17.8-1
# Thu, 17 Nov 2022 01:50:56 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:50:56 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:50:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Nov 2022 02:32:16 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:32:16 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:32:16 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:32:16 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:32:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:32:22 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:32:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:32:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:32:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:32:23 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:32:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:32:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef215ea8d074f0c94eaca01c6b06d36fb0f4c6fba48ee0ef78e27af949e1d2b`  
		Last Modified: Thu, 17 Nov 2022 01:55:26 GMT  
		Size: 147.8 MB (147769396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcca442805e3b737009449270c196f790833773cbc162dc0079707eb9a15ae9f`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 3.6 MB (3641327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1e00f3752e3320f2375e9fac4e606e961ab5738c114f1cf43f1c25dd66366`  
		Last Modified: Thu, 17 Nov 2022 02:35:28 GMT  
		Size: 8.7 MB (8739498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6c6842d25068d8c1f061d8c345cfde396866e4bb5af072b98ae5ac310c098`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4103a3371d8ed261215075ecabcac36c8dab859df24a6e34018af6c1709671d`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b30115ed998a5f308df27be48a7b6c341323c421cb46866a35963513fcfa7b06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221260736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4fff7644a190477867153a4142c8fa294884b4f0a8ac554343f9d3801402ae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:59:23 GMT
ARG version=11.0.17.8-1
# Fri, 16 Dec 2022 00:59:42 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 00:59:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 00:59:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Dec 2022 01:22:15 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 16 Dec 2022 01:22:15 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 16 Dec 2022 01:22:15 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Dec 2022 01:22:15 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 16 Dec 2022 01:22:15 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 16 Dec 2022 01:22:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 16 Dec 2022 01:22:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Dec 2022 01:22:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Dec 2022 01:22:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 16 Dec 2022 01:22:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 16 Dec 2022 01:22:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Dec 2022 01:22:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aade9a94f7c23d8fc79b4c11ce14d37b8569a6fec3017a295169ff500ec8d8`  
		Last Modified: Fri, 16 Dec 2022 01:03:43 GMT  
		Size: 144.9 MB (144905924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f97abaac636b83c48901a954aad2590cc61f80cced9b27aa8d43b44f43a9f30`  
		Last Modified: Fri, 16 Dec 2022 01:24:38 GMT  
		Size: 3.6 MB (3649884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33db164bd6b73340003cd55423a8dd5849cc7a487cc94c2bb357ccc1a8dc3ca1`  
		Last Modified: Fri, 16 Dec 2022 01:24:38 GMT  
		Size: 8.7 MB (8739505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fbf8565a1c4b4d0234f157780196cad6f3c6da31c3715376cf33e20181ae58`  
		Last Modified: Fri, 16 Dec 2022 01:24:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeee5a1b81e9a2419e7b0709853995c8c8d8143e3577a8ad85dc85ba657e485`  
		Last Modified: Fri, 16 Dec 2022 01:24:37 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
