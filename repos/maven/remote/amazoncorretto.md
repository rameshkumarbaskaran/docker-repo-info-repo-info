## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:4a07acfd6a04729d463aeb38719158aa5215093fa8b883622807ba5c1f8a32b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c5a2c6a62677c74498f6f591b1cddaa72644a785c2ce489fb39207bd01ad6bfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221621255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d757549fbc7b73ad113422166b35094b8f8849eb933be1d65e3067090ef905e6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 00:03:17 GMT
ARG version=11.0.15.9-1
# Wed, 22 Jun 2022 00:03:41 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 00:03:42 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 00:03:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Jun 2022 02:39:09 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 22 Jun 2022 02:39:10 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 22 Jun 2022 02:39:10 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Jun 2022 02:39:10 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 22 Jun 2022 02:39:10 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 22 Jun 2022 02:39:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Jun 2022 02:39:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Jun 2022 02:39:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Jun 2022 02:39:18 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Jun 2022 02:39:18 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Jun 2022 02:39:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Jun 2022 02:39:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39ce0867db86a4afbb61ab483727e3431b7b5cfdb6411d702ff57f93fdbcb53`  
		Last Modified: Wed, 22 Jun 2022 00:07:22 GMT  
		Size: 147.0 MB (146960185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93aa8443a82f86e5a78c3909dc1902934bef3889b4d2c607ca80de7b5c1b580`  
		Last Modified: Wed, 22 Jun 2022 02:42:15 GMT  
		Size: 3.6 MB (3625395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a141c4b22405913b26c4dffab3729665789a50e069968a8d7b591c83b69ffe3c`  
		Last Modified: Wed, 22 Jun 2022 02:42:15 GMT  
		Size: 8.7 MB (8739491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e174f1cf0f0d789d5afff8e3401ea88d8f2f0d19e9e1a40ba98b8fda995782`  
		Last Modified: Wed, 22 Jun 2022 02:42:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87528388f672a162bb4b51957d9ce6269e07ecda0d7d90e6e25b041d66663cf3`  
		Last Modified: Wed, 22 Jun 2022 02:42:14 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4f1e376c4250262cfd25b42e3804456583e2115bd5b608489560462fc6fed5ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220475273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b835035e13affde1d0fe9cdc4137559d96759e918f25b659588b17043899afca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 01:01:55 GMT
ARG version=11.0.15.9-1
# Wed, 22 Jun 2022 01:02:15 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 01:02:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 01:02:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Jun 2022 04:37:05 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 22 Jun 2022 04:37:06 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 22 Jun 2022 04:37:07 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Jun 2022 04:37:08 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 22 Jun 2022 04:37:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 22 Jun 2022 04:37:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Jun 2022 04:37:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Jun 2022 04:37:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Jun 2022 04:37:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Jun 2022 04:37:24 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Jun 2022 04:37:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Jun 2022 04:37:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5244c1161f4e2219c158b77dfd28376de2ea03be60029bd422900706b0e4d0`  
		Last Modified: Wed, 22 Jun 2022 01:04:29 GMT  
		Size: 144.2 MB (144186875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90614fcccc53fa86643cc29e5bded2de8856641911b71238a81d6e14142e8d7`  
		Last Modified: Wed, 22 Jun 2022 04:41:31 GMT  
		Size: 3.6 MB (3629078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424f181a19192cb4d12238939ed1adb61911d2a57789363ef465cbd6a6c1495`  
		Last Modified: Wed, 22 Jun 2022 04:41:31 GMT  
		Size: 8.7 MB (8739464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd96263c620d2227c981ad55dd05d98c03bab79bd768b31a6b4dc59e07ee6d46`  
		Last Modified: Wed, 22 Jun 2022 04:41:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae6f9e1dfe1431d4ec2bb4e1487e91e79cdad930f053e6d87c29e4f8cbb846`  
		Last Modified: Wed, 22 Jun 2022 04:41:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
