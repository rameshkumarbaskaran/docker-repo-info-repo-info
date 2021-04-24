## `maven:3-amazoncorretto-16`

```console
$ docker pull maven@sha256:2f0606c369420c4688de74ac45dfeaa6903d6a76dd553a235963d9abefb4aaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-16` - linux; amd64

```console
$ docker pull maven@sha256:666a32f97d8dc16e373e1eff18454f23d3fa223092ba8463bb5dea7dfbf38a96
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235065850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0111869b4471ae405aa9ce622eb17ca2dbe45b2a8cfd1d0d62dc77917a78477`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:20 GMT
ADD file:3b750ce7e7425c1cb02261d65b1e301d5818cda51a80dc8ab3b915ee5ca37d4e in / 
# Tue, 30 Mar 2021 21:59:21 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 04:40:59 GMT
ARG version=16.0.1.9-1
# Sat, 24 Apr 2021 04:41:21 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 24 Apr 2021 04:41:21 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 04:41:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Sat, 24 Apr 2021 04:46:37 GMT
ARG MAVEN_VERSION=3.8.1
# Sat, 24 Apr 2021 04:46:37 GMT
ARG USER_HOME_DIR=/root
# Sat, 24 Apr 2021 04:46:38 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Sat, 24 Apr 2021 04:46:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Sat, 24 Apr 2021 04:46:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Sat, 24 Apr 2021 04:46:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 24 Apr 2021 04:46:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 24 Apr 2021 04:46:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 24 Apr 2021 04:46:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 24 Apr 2021 04:46:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 24 Apr 2021 04:46:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 24 Apr 2021 04:46:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:99a21848b482c10fd4b103b7ab95e1446142e76e3dfa673efd0a23fb264ec5e5`  
		Last Modified: Tue, 30 Mar 2021 13:54:37 GMT  
		Size: 61.9 MB (61946585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639469cf55fb09ef9908b91956cac3b435540b062229048ead336526abc3546e`  
		Last Modified: Sat, 24 Apr 2021 04:42:30 GMT  
		Size: 160.0 MB (159957954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65aa20537b150a96b2604fdc84c91087d840c0f1b47742679ace70a88ab9571d`  
		Last Modified: Sat, 24 Apr 2021 04:52:29 GMT  
		Size: 3.5 MB (3549154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767994b0c7c9a23d30c978e4ff9727b2f2c20db53cad2efc1d31202c82c5a4bf`  
		Last Modified: Sat, 24 Apr 2021 04:52:30 GMT  
		Size: 9.6 MB (9610948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edfb40deeab9391af2fe1e54632cc41e0e5241833238e339060f73dbd532d18`  
		Last Modified: Sat, 24 Apr 2021 04:52:28 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dbcddae06e8aa81f8a9da6548d1e522332ebc6e47c018e9f3d306a802a32b0`  
		Last Modified: Sat, 24 Apr 2021 04:52:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:136ef713bc5f97a6ae1a80b0e8670a421f4a5b0a5c55dc1397055a19242bbd0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236787221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4302e9ec2f440479dead41626905d99642c80c696e73963598eec095a3166dfb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 02:15:31 GMT
ARG version=16.0.1.9-1
# Sat, 24 Apr 2021 02:16:07 GMT
# ARGS: version=16.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 24 Apr 2021 02:16:10 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 02:16:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Sat, 24 Apr 2021 03:01:36 GMT
ARG MAVEN_VERSION=3.8.1
# Sat, 24 Apr 2021 03:01:37 GMT
ARG USER_HOME_DIR=/root
# Sat, 24 Apr 2021 03:01:38 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Sat, 24 Apr 2021 03:01:39 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Sat, 24 Apr 2021 03:01:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Sat, 24 Apr 2021 03:01:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 24 Apr 2021 03:01:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 24 Apr 2021 03:02:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 24 Apr 2021 03:02:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 24 Apr 2021 03:02:02 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 24 Apr 2021 03:02:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 24 Apr 2021 03:02:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21f9218d896bed8769806cdadee02297ffea4768446608aab77c1fedf6b8acb`  
		Last Modified: Sat, 24 Apr 2021 02:17:03 GMT  
		Size: 159.9 MB (159921257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9179211999750173824e5e7d09f6951bcc960397952e4ee525573ca5b100fb9d`  
		Last Modified: Sat, 24 Apr 2021 03:04:57 GMT  
		Size: 3.6 MB (3593776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccee14a2f4839f7352431199c6d157455c11bd5f5a855adfa0eb383f6b200f6`  
		Last Modified: Sat, 24 Apr 2021 03:04:58 GMT  
		Size: 9.6 MB (9610936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837664c6c8f2de1cd7c086aec9242e1d511e5b5b7571e0f43dcd16a17085dece`  
		Last Modified: Sat, 24 Apr 2021 03:04:56 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b385bd6e47618aca8e1c8a439d85a2aa2c29d00b963da83e6ca11b8698f75a2`  
		Last Modified: Sat, 24 Apr 2021 03:04:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
