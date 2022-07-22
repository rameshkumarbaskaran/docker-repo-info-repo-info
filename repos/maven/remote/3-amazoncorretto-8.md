## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:e8cc8d6950c06b31777df029fe8ac65e18ab1dcbcfadd528be16f00677937465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:2ec383f237c25425561bc7b0e154b665247376b6f212d4af19e29c5a0fdf4c3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150223869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899c5bb9ebb2566d754a3738edda879460bff6e5e135e94501a60472e792f819`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Fri, 22 Jul 2022 18:19:30 GMT
ARG version=1.8.0_342.b07-3
# Fri, 22 Jul 2022 18:19:52 GMT
# ARGS: version=1.8.0_342.b07-3
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jul 2022 18:19:52 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jul 2022 18:19:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 Jul 2022 18:41:56 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 22 Jul 2022 18:41:57 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 22 Jul 2022 18:41:57 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Jul 2022 18:41:57 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 22 Jul 2022 18:41:57 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 22 Jul 2022 18:41:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 22 Jul 2022 18:41:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Jul 2022 18:41:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Jul 2022 18:41:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 Jul 2022 18:41:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 22 Jul 2022 18:41:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 22 Jul 2022 18:41:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Jul 2022 18:41:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69754eaed5c3743c6dcfa3541a20d2b8c3a5b937ca0ce61ec098d03fb7996c67`  
		Last Modified: Fri, 22 Jul 2022 18:22:44 GMT  
		Size: 75.6 MB (75557973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c899bf62b4730ea9080802a534c7b935ca8c3cb6aecc7a0ae54f95127ae551`  
		Last Modified: Fri, 22 Jul 2022 18:44:14 GMT  
		Size: 3.6 MB (3630214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e666b8e575e5aabaf8884a53fe181b6c1646a69ed72a4952c76dfe58329e5436`  
		Last Modified: Fri, 22 Jul 2022 18:44:14 GMT  
		Size: 8.7 MB (8739491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086f29ba490fa7aa25f818867d170e443917612b1b2e75b9e9f4b3c524944908`  
		Last Modified: Fri, 22 Jul 2022 18:44:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0302b078effe72d0be99f5aed0ac1b3168400a45ce7b371be974fc9ebd9be8e7`  
		Last Modified: Fri, 22 Jul 2022 18:44:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:67b36779853ad4c11ef1de33df882cf836a774a2eac549c097cc745301251ce1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135883234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178811ca8c08aa51df8c124614a0a359b006c99f234cd662ddf0487fea358354`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Fri, 22 Jul 2022 18:39:25 GMT
ARG version=1.8.0_342.b07-3
# Fri, 22 Jul 2022 18:39:37 GMT
# ARGS: version=1.8.0_342.b07-3
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jul 2022 18:39:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jul 2022 18:39:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 Jul 2022 18:58:35 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 22 Jul 2022 18:58:35 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 22 Jul 2022 18:58:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Jul 2022 18:58:37 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 22 Jul 2022 18:58:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 22 Jul 2022 18:58:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 22 Jul 2022 18:58:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Jul 2022 18:58:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Jul 2022 18:58:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 Jul 2022 18:58:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 22 Jul 2022 18:58:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 22 Jul 2022 18:58:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Jul 2022 18:58:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82b73c98cf8c8bcfa116da3fe9f01d1cd4b2ebe491e6235a2343496623f62f3`  
		Last Modified: Fri, 22 Jul 2022 18:40:49 GMT  
		Size: 59.6 MB (59591976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50159290c4a8341b7bc34fc41a27b94f93dc1b808905273beff511a748651157`  
		Last Modified: Fri, 22 Jul 2022 19:02:11 GMT  
		Size: 3.6 MB (3631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021e1ec01d8bd01d111a878fcc73f405be82dde63fc4c17f8755cc60b8cedb91`  
		Last Modified: Fri, 22 Jul 2022 19:02:11 GMT  
		Size: 8.7 MB (8739472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d860dc9e151eb38103fae9a3dc1b8b7a2d74710d893a7b14ac963d58ffdf6969`  
		Last Modified: Fri, 22 Jul 2022 19:02:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04f73d35c9787fc976832d4aa1bbda1bc5cf1ade64051574c247f117ca1ce7`  
		Last Modified: Fri, 22 Jul 2022 19:02:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
