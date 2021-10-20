## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:79195ae8459054f624137495ee0b467802e209be12e8855d5a5eeb183e8ebb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b2976f3510e6c3400a6d2b48c9e5e6614e882c8c9220b0d491d69bed39b3b471
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150009886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb645cc1746790bf64712c2fa74691618c7f2514864158f5f4a736437b422f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:20:20 GMT
ADD file:21dc1ad70daefae1cf0e1b3e78fab06decda5cb9bc958d8a178adb3eddd1fb32 in / 
# Fri, 01 Oct 2021 21:20:20 GMT
CMD ["/bin/bash"]
# Wed, 20 Oct 2021 18:19:24 GMT
ARG version=1.8.0_312.b07-1
# Wed, 20 Oct 2021 18:19:47 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Oct 2021 18:19:48 GMT
ENV LANG=C.UTF-8
# Wed, 20 Oct 2021 18:19:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 20 Oct 2021 18:45:47 GMT
ARG MAVEN_VERSION=3.8.3
# Wed, 20 Oct 2021 18:45:47 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 Oct 2021 18:45:48 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Wed, 20 Oct 2021 18:45:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Wed, 20 Oct 2021 18:45:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 20 Oct 2021 18:46:05 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 20 Oct 2021 18:46:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 Oct 2021 18:46:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 Oct 2021 18:46:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 20 Oct 2021 18:46:06 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 20 Oct 2021 18:46:06 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 20 Oct 2021 18:46:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 Oct 2021 18:46:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0728ce74490afacced1ac863ee989913071f97c52ab996e46cdd6b5369a2d63a`  
		Last Modified: Fri, 01 Oct 2021 10:54:14 GMT  
		Size: 62.0 MB (61952638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418b0cae534ccf0aa47ebf2692e9e9af818e76138529c6cb3e67dbcc04da4499`  
		Last Modified: Wed, 20 Oct 2021 18:23:22 GMT  
		Size: 75.4 MB (75351284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353e34398399044e327171f6b8877d5730e7438e126ba6f1977d262daec0e8fa`  
		Last Modified: Wed, 20 Oct 2021 18:48:59 GMT  
		Size: 3.6 MB (3599124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27805d5b38d64bda0aac9afa8f61652dc90997bd358a8c47aa1ba790e4bfada8`  
		Last Modified: Wed, 20 Oct 2021 18:49:00 GMT  
		Size: 9.1 MB (9105627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa060ea9211a9c2f3d36e27ae534fcca7c206a783cda8c9ef107804963c631ca`  
		Last Modified: Wed, 20 Oct 2021 18:48:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179c44ae774e6d6416d50fc606d637c05565f7a5eef185b50298f792e02f3bdd`  
		Last Modified: Wed, 20 Oct 2021 18:48:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8c29a375dff58ea05a1f8e4997111e114673fcb898d0f00110cf2565b90c0bef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135665345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0d2776c9ae17f3aa6bee05adb8d005e199857611ab8e6fd803d662c28e3b47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:39:54 GMT
ADD file:1d2ae2bfc4c1f83dc53f48b42503812d345622ab95d8fc84536216ef3d53d807 in / 
# Fri, 01 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:57:32 GMT
ARG version=1.8.0_302.b08-1
# Fri, 01 Oct 2021 21:57:50 GMT
# ARGS: version=1.8.0_302.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:57:50 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:57:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 13 Oct 2021 08:14:40 GMT
ARG MAVEN_VERSION=3.8.3
# Wed, 13 Oct 2021 08:14:40 GMT
ARG USER_HOME_DIR=/root
# Wed, 13 Oct 2021 08:14:41 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Wed, 13 Oct 2021 08:14:42 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Wed, 13 Oct 2021 08:14:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 13 Oct 2021 08:15:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 13 Oct 2021 08:15:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 13 Oct 2021 08:15:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 13 Oct 2021 08:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 13 Oct 2021 08:15:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 13 Oct 2021 08:15:13 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 13 Oct 2021 08:15:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 13 Oct 2021 08:15:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5aa4871be3ec1bcadf7a5257231adc7740edac9a612749884f03ab14b4b2d4ec`  
		Last Modified: Fri, 01 Oct 2021 16:32:04 GMT  
		Size: 63.6 MB (63581978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59aa11c1c46065f0e96c13fcd24b5d373b0d7152e74ec2eaa61aa3c0582ede4`  
		Last Modified: Fri, 01 Oct 2021 22:00:20 GMT  
		Size: 59.4 MB (59393641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ffca212fd7fd29d0ee08ce866a6e4b68f6ec0fa3683c4152141299672a8f2`  
		Last Modified: Wed, 13 Oct 2021 08:25:41 GMT  
		Size: 3.6 MB (3582909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f200407f21f1dad319c82248315311c407e97f2705c3492c60e9822bf98062bb`  
		Last Modified: Wed, 13 Oct 2021 08:25:42 GMT  
		Size: 9.1 MB (9105601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1728f10412d81af8885eccf394c89f309d134171286b6c5527384075ab80c7`  
		Last Modified: Wed, 13 Oct 2021 08:25:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af47321f95c33e3b563e52556f1f131a12843c97f41523e4f3c02081067d0059`  
		Last Modified: Wed, 13 Oct 2021 08:25:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
