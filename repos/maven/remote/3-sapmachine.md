## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:5b8e7d03e28b1770a30be9dbe29b44ac706312b975e81d72e263f2763a3ce59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:2db7585c46ca3fcec89ec99d187ad97a1314b526682d11ff6f3ca2c5a64a0218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275387423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80e2a361d04f5d4320d98b316f0158407021320709d02702f0cc09f9c18e26c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:38:43 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:38:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 13 Oct 2023 08:38:44 GMT
CMD ["jshell"]
# Fri, 22 Sep 2023 08:38:46 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 22 Sep 2023 08:38:46 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Sep 2023 08:38:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Sep 2023 08:38:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Sep 2023 08:38:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f425e71ec5858106063bc89a7cd5a4d7637241befc60778ed6829ffc6dce84`  
		Last Modified: Fri, 13 Oct 2023 08:46:06 GMT  
		Size: 214.6 MB (214609554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58f21d3b62429781d09bc2d44529dd29cc2d10046a7c5bc37dde23d50daeb1f`  
		Last Modified: Fri, 13 Oct 2023 10:04:53 GMT  
		Size: 20.9 MB (20930981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1f27e693bb3557386ae0ba4816ff7d5aa31fc6c0aa586bf557b8ff1e740e40`  
		Last Modified: Fri, 13 Oct 2023 10:04:50 GMT  
		Size: 9.4 MB (9406415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d6a623173dcf4c68972a1393d0dd01a9c8fa0c7b76a929a77f229c741de9d2`  
		Last Modified: Fri, 13 Oct 2023 10:04:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87ef055c0a5de410ec1650720ec4a1b70ec4fd686f60cec1792ecd1853b1538`  
		Last Modified: Fri, 13 Oct 2023 10:04:49 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dae48343765368f17128391bb3622bf868f9efa1a8e6ce1296375f9ae026085`  
		Last Modified: Fri, 13 Oct 2023 10:04:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:24dcefa614bf5a26bcf72f62bc27ce5a2f88f8ece313a3d3f67cfb71df161304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256954896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66e1d3980cc910c07b9f0bb550164791e439d10851c9e1499fff440f63d9c0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:01:44 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.8.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:01:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 13 Oct 2023 03:01:46 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c9ee343e48bb3c49e462495a65652e9c7a442106e88a173b9ec87e0465c427`  
		Last Modified: Fri, 13 Oct 2023 03:08:09 GMT  
		Size: 198.2 MB (198246532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d7cd68b24634d276bcde9c6e0340c0527aacd7711d2fa0938eb4e87b63eb44`  
		Last Modified: Fri, 13 Oct 2023 08:24:00 GMT  
		Size: 20.9 MB (20908602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152efb505f3b1da032bbe847b16602c12a0f7675f182c5ddf404315cd6048b0a`  
		Last Modified: Fri, 13 Oct 2023 08:23:58 GMT  
		Size: 9.4 MB (9406460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38742720cedd40475c035aedb060c00e5b4268b3cc577a6552b523afc0d16808`  
		Last Modified: Fri, 13 Oct 2023 08:23:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe1e2425a2718f119f6eb4ff9ce37711af57205c5094730d0a57833a2f3e223`  
		Last Modified: Fri, 13 Oct 2023 08:23:57 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab24b061d3cb07f826f463500c2324c63f5f4c9c0345628cb7f9aea252194d4a`  
		Last Modified: Fri, 13 Oct 2023 08:23:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:086cb50643142116f993731bc2da49c4e60a78141027d8e27eb1bc98c34d6f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285441381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8ba61cde50909545f721d006813cea71b1445022908efb3f7ca7e199a96b7d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 06:45:00 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 13 Oct 2023 06:45:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 13 Oct 2023 06:45:07 GMT
CMD ["jshell"]
# Fri, 22 Sep 2023 08:38:46 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 Sep 2023 08:38:46 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 22 Sep 2023 08:38:46 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Sep 2023 08:38:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Sep 2023 08:38:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Sep 2023 08:38:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a33a4ccb190db1ba22731942f2d5c3e93d0ff961532e41ffd83116e2ecedd`  
		Last Modified: Fri, 13 Oct 2023 06:52:44 GMT  
		Size: 216.0 MB (216005918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a5eba44b244c0740e3787ccc193f13415d242a57112d87944b79ee8b14f12e`  
		Last Modified: Fri, 13 Oct 2023 08:35:01 GMT  
		Size: 24.3 MB (24344868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f09f4068439d3e27ce687f309259bc0851436699a3207580f0d40e80e342d83`  
		Last Modified: Fri, 13 Oct 2023 08:34:56 GMT  
		Size: 9.4 MB (9406432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496cd65c064978c111b7acf5917015bf33a69f932a2f07ba53e777b24a1e375f`  
		Last Modified: Fri, 13 Oct 2023 08:34:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63019d5fb45cb5827c55e525aa53fd3f3c7af9441d487495711df29d5319ddd`  
		Last Modified: Fri, 13 Oct 2023 08:34:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1316fa5d6635dfb38b5e68ec601e531262464abda8e8a59704739e9207f27b`  
		Last Modified: Fri, 13 Oct 2023 08:34:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
