## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:44f9a2b0f1e79f19ee61995ce5051c4ddf13c665cb66c1fcff32bee1530a5a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:8f9af2f21715834ce03cb27dd9dbaf0e9fa0f97d4dd5cfadff19997a20e48aed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221471974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab380f75584c314b7e28f0dd08d1246e9fd2a8ff08550916109e06c0b6204aa3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 22:09:19 GMT
ARG version=11.0.14.9-1
# Wed, 13 Apr 2022 22:09:50 GMT
# ARGS: version=11.0.14.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 13 Apr 2022 22:09:50 GMT
ENV LANG=C.UTF-8
# Wed, 13 Apr 2022 22:09:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 13 Apr 2022 22:31:42 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 13 Apr 2022 22:31:42 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 13 Apr 2022 22:31:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 13 Apr 2022 22:31:43 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 13 Apr 2022 22:31:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 13 Apr 2022 22:31:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 13 Apr 2022 22:31:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 13 Apr 2022 22:31:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 13 Apr 2022 22:31:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 13 Apr 2022 22:31:49 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 13 Apr 2022 22:31:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 13 Apr 2022 22:31:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3645737f83fa7aac468235fbeb688e0197b88148de741dc2363726702f882c33`  
		Last Modified: Wed, 13 Apr 2022 22:13:43 GMT  
		Size: 146.9 MB (146872055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e678e6923b9b447734f4deddd3d2e65f70265c82e9854a6e92eb3e0a027b0f4`  
		Last Modified: Thu, 14 Apr 2022 00:05:35 GMT  
		Size: 3.6 MB (3624677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb5bbf089928ec836d46e9525fba79ef67270a190cabce71331972e41c4447`  
		Last Modified: Thu, 14 Apr 2022 00:05:35 GMT  
		Size: 8.7 MB (8736390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44de08ea269540acb52a609155819f53623c4c8d10a3471d46a1febe0fa8de`  
		Last Modified: Thu, 14 Apr 2022 00:05:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9825097bcad8757ec3e997968ed9b32b7614dc7f79758155b8a87edb03e056e7`  
		Last Modified: Thu, 14 Apr 2022 00:05:34 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3ab467c6580129d5a934b18cc21a6ece424d4fb2c164b77fc390d8818918b6f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220440423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bd026f82d8d2d68f8b16042989db0c6af0bc0d8a18324b36c5a535eef45c3b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 19 Apr 2022 21:39:43 GMT
ARG version=11.0.15.9-1
# Tue, 19 Apr 2022 21:40:01 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 19 Apr 2022 21:40:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 21:40:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 19 Apr 2022 23:03:12 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 19 Apr 2022 23:03:12 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 19 Apr 2022 23:03:13 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Apr 2022 23:03:14 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 19 Apr 2022 23:03:15 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 19 Apr 2022 23:03:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 19 Apr 2022 23:03:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Apr 2022 23:03:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Apr 2022 23:03:29 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 19 Apr 2022 23:03:30 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 19 Apr 2022 23:03:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Apr 2022 23:03:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85077095d5a2c473594b77c6d23a963d73bf0a7e6accf188af15b4161ddc8213`  
		Last Modified: Tue, 19 Apr 2022 21:42:31 GMT  
		Size: 144.2 MB (144188940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f55976e184036f7ff9d1a30184d0e4c9d0104718fd2f6959befd4539e1bbc8`  
		Last Modified: Tue, 19 Apr 2022 23:07:40 GMT  
		Size: 3.6 MB (3643650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bb9b6da72a70b8086e299f4cc239ceb0d77955e5b4c097072a8d3297a9b150`  
		Last Modified: Tue, 19 Apr 2022 23:07:40 GMT  
		Size: 8.7 MB (8736336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b755f793293fce190911e078f5815083de1d5e23d621fb4158caa0f2665ef6`  
		Last Modified: Tue, 19 Apr 2022 23:07:39 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1caab8c9db0da2841be4606628ba047236672544b63b2a81cf8f3804a9d0c97`  
		Last Modified: Tue, 19 Apr 2022 23:07:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
