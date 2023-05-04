<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:2.2`](#orientdb22)
-	[`orientdb:2.2.37`](#orientdb2237)
-	[`orientdb:2.2.37-spatial`](#orientdb2237-spatial)
-	[`orientdb:3.0`](#orientdb30)
-	[`orientdb:3.0-tp3`](#orientdb30-tp3)
-	[`orientdb:3.0.44`](#orientdb3044)
-	[`orientdb:3.0.44-tp3`](#orientdb3044-tp3)
-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.18`](#orientdb3218)
-	[`orientdb:3.2.18-tp3`](#orientdb3218-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:64fcdfaf9fc93ff47d53ecfb25c94bb4ce0a8c51dde59733cbdd57da00491e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:193d4069c86b0fbe6141a0af39d77ab5a5df717696cbf6033652d65ee8024a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144054763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3e4f27f5413862a9a3b62ca10c283d2f3488d15513f35e5670b70e2adcfeae`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:64fcdfaf9fc93ff47d53ecfb25c94bb4ce0a8c51dde59733cbdd57da00491e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:193d4069c86b0fbe6141a0af39d77ab5a5df717696cbf6033652d65ee8024a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144054763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3e4f27f5413862a9a3b62ca10c283d2f3488d15513f35e5670b70e2adcfeae`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:2d8c7edd9cc74afca433373fcdfb95f05866a00be63675412ffc9c30fc4a6534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:52b2133293a58b084ba98d4d925f43ceac3f599bb96d051c18381a6daac01ecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145257361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bab68eda90affb614127ee59d481dc0411be5c9abc31b469c4d508641c3df9`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Thu, 04 May 2023 15:25:24 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73c6bebaf8a953ffeb35acbeedbe2552849a92c2afee264a2986fc1b7ed8dca`  
		Last Modified: Thu, 04 May 2023 15:27:04 GMT  
		Size: 1.2 MB (1202598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:cbefe268b9b3da5eaa1f0546207d3ecc9f44bcf130753491e73338675cfff8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:069c835f950043ee985e14b210279f659742e5627e59b6ba5cca31485e0c0eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134645686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce2460f59fcf407115ee388f86e13c88e178643ba77c3c7abd73f5c302c06`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Thu, 04 May 2023 15:24:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:00 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:01 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca78bb78f397024fa509b4d7126fdd2443c4bdaa5f70e84013515deed6b4fa`  
		Last Modified: Thu, 04 May 2023 15:26:31 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69358d9afc82485abe8b4ebfe75206801459a1c9593787a22158477adc19e1f`  
		Last Modified: Thu, 04 May 2023 15:26:33 GMT  
		Size: 37.1 MB (37064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:99f5b647a2f9ec81937538fa79e6a984eb97f6644adcd471c4f9281500a22420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:13c968ac755542c1f8f14896b28a2541006dcabae26f35ff3bca66deb4360ab0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161666008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b170d11a08bca919aca70ec93c00f02601fc783db1f744832011a1c2bc2a26`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Thu, 04 May 2023 15:25:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:12 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:25:12 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:12 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:12 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:25:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4989cbb19e207dd073649d73014a93b89c4d4d9a4f6f6ba9b9e2275daf640f`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9826a8b6d27ac72ae8f7cc52449fc3c8bee8c616f2382593a858e9f55bc26`  
		Last Modified: Thu, 04 May 2023 15:26:45 GMT  
		Size: 64.1 MB (64083764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccf42b9644f34cd8dd55b94ed3e7c14e0d8c6931271e7b8c2c54c377ad273c8`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44`

```console
$ docker pull orientdb@sha256:cbefe268b9b3da5eaa1f0546207d3ecc9f44bcf130753491e73338675cfff8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44` - linux; amd64

```console
$ docker pull orientdb@sha256:069c835f950043ee985e14b210279f659742e5627e59b6ba5cca31485e0c0eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134645686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce2460f59fcf407115ee388f86e13c88e178643ba77c3c7abd73f5c302c06`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Thu, 04 May 2023 15:24:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:00 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:01 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca78bb78f397024fa509b4d7126fdd2443c4bdaa5f70e84013515deed6b4fa`  
		Last Modified: Thu, 04 May 2023 15:26:31 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69358d9afc82485abe8b4ebfe75206801459a1c9593787a22158477adc19e1f`  
		Last Modified: Thu, 04 May 2023 15:26:33 GMT  
		Size: 37.1 MB (37064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44-tp3`

```console
$ docker pull orientdb@sha256:99f5b647a2f9ec81937538fa79e6a984eb97f6644adcd471c4f9281500a22420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:13c968ac755542c1f8f14896b28a2541006dcabae26f35ff3bca66deb4360ab0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161666008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b170d11a08bca919aca70ec93c00f02601fc783db1f744832011a1c2bc2a26`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Thu, 04 May 2023 15:25:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:12 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:25:12 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:12 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:12 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:25:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4989cbb19e207dd073649d73014a93b89c4d4d9a4f6f6ba9b9e2275daf640f`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9826a8b6d27ac72ae8f7cc52449fc3c8bee8c616f2382593a858e9f55bc26`  
		Last Modified: Thu, 04 May 2023 15:26:45 GMT  
		Size: 64.1 MB (64083764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccf42b9644f34cd8dd55b94ed3e7c14e0d8c6931271e7b8c2c54c377ad273c8`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:36e130ec58149ed8fc02439581faaa176b311e6851151149bb54088e69adcf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:2c485f85cbbdc8b0236c5fff1d9536389372a8b94ce9c33fbec288f4ccc1d57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150662066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cde820b9f00f1e7378a48e3f6c079a5ee72267574cef6cf0ae06d4cc1bba2d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:31 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:35 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:35 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:36 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:36 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:36 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9295cac4efc25743ced255915288067abb70682db3c510691669eb39c55e5`  
		Last Modified: Thu, 04 May 2023 15:26:07 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602cb6ba2d624fd2f33952d261c603d5a42cdb526d12e681c86ea960dbf1f27`  
		Last Modified: Thu, 04 May 2023 15:26:10 GMT  
		Size: 53.1 MB (53081198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:0d13dea248cccfccdb2a846564eaa6e2d5b8dbbfac1bac254bed77c4e6d9d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a59381a9b847f690e20b52dda8902c8227d04064107bdd1a453df5d0fba29fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e47bb2dc5207000b5a8bca959763712a51cb447b709965623871a3584a038d8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:49 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:24:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:49 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:49 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000666c8516011f72b54bc17f9d750bb1c0122904cf9d607fc51d175896a1c6`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f10d6d9a7c31fbf513aff4f5d6d34a67fc04e55a481d6f9bdfa5293cda1d5c`  
		Last Modified: Thu, 04 May 2023 15:26:22 GMT  
		Size: 76.1 MB (76086848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f833b219c82fd8d27f736d549700515305c20a29ec3f810e4110807b0518be0f`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:36e130ec58149ed8fc02439581faaa176b311e6851151149bb54088e69adcf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:2c485f85cbbdc8b0236c5fff1d9536389372a8b94ce9c33fbec288f4ccc1d57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150662066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cde820b9f00f1e7378a48e3f6c079a5ee72267574cef6cf0ae06d4cc1bba2d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:31 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:35 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:35 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:36 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:36 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:36 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9295cac4efc25743ced255915288067abb70682db3c510691669eb39c55e5`  
		Last Modified: Thu, 04 May 2023 15:26:07 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602cb6ba2d624fd2f33952d261c603d5a42cdb526d12e681c86ea960dbf1f27`  
		Last Modified: Thu, 04 May 2023 15:26:10 GMT  
		Size: 53.1 MB (53081198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:0d13dea248cccfccdb2a846564eaa6e2d5b8dbbfac1bac254bed77c4e6d9d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a59381a9b847f690e20b52dda8902c8227d04064107bdd1a453df5d0fba29fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e47bb2dc5207000b5a8bca959763712a51cb447b709965623871a3584a038d8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:49 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:24:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:49 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:49 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000666c8516011f72b54bc17f9d750bb1c0122904cf9d607fc51d175896a1c6`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f10d6d9a7c31fbf513aff4f5d6d34a67fc04e55a481d6f9bdfa5293cda1d5c`  
		Last Modified: Thu, 04 May 2023 15:26:22 GMT  
		Size: 76.1 MB (76086848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f833b219c82fd8d27f736d549700515305c20a29ec3f810e4110807b0518be0f`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:015b42ff02e128806d681d304b77c2d1c277503a83a4145f2571a209fc58644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:371ca05cf3a787b97e237139828e3853ea0396ce80658e54e1281d70b964a360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161698471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec79a4d1a5bd908b7f8c80be8b60fd152581df754fbee215a9041e08e9ae4c8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 15:24:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:13 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:13 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:13 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:13 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a369a4a53bfe75f0c7a153b6ae4e9d3baa988889cc13eab8f7a9bce36d3fea`  
		Last Modified: Thu, 04 May 2023 15:25:39 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c28b9a56815881546f634776daa23f47bfacfb23ac30b5a2406eef9201df26`  
		Last Modified: Thu, 04 May 2023 15:25:43 GMT  
		Size: 64.1 MB (64117603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c96c8fd6845c6f5fa215bcdbc222ad91aadb8ad11564769cf4be22359c666fb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153515537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ad7af142600c43403751a5d07fa068013886c301a40b3eca13f0451c97cf25`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:52:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:52:06 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:52:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:52:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 11:49:51 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 11:49:51 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 11:49:55 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:49:59 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 11:49:59 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:49:59 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 11:49:59 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2424
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2480
# Thu, 04 May 2023 11:50:00 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe39f2d222e718fa2fcf09ffc515022b8134ad2bd86f1eade8de914c8b900e5`  
		Last Modified: Thu, 04 May 2023 06:54:34 GMT  
		Size: 12.1 MB (12066173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e637393c956ae291142bb334658dcc4041571b8ec39500ad13c11acd6d4b93`  
		Last Modified: Thu, 04 May 2023 06:54:39 GMT  
		Size: 50.3 MB (50304911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a09d7f45da0bae2c893dc41b117962a9dcdbd589e6fd5caeb3e25f194c3d6d`  
		Last Modified: Thu, 04 May 2023 06:54:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924586c2893e089e4558ef6681218c1d10ce60496ebe1c552da7cfe645816ebd`  
		Last Modified: Thu, 04 May 2023 11:50:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f6c35c6787ff833785be548c2bbd673122f545a6d153679668ac7ce2be587`  
		Last Modified: Thu, 04 May 2023 11:50:28 GMT  
		Size: 64.1 MB (64117612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:59b19f96d8495998a9151188f2db85e879e30466464eb699d2ea044099aae178
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158715442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfdcb2dce484053fc8078d13095615aa83779cc4923415bbff27bac733b02df`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 12:07:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 12:07:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 12:07:35 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:07:38 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 12:07:39 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:07:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 12:07:39 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2424
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2480
# Thu, 04 May 2023 12:07:39 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c1cae9037b6c50ec0e053161e5ec3654c581e3b9d0f3dd60da90f7e1af01b5`  
		Last Modified: Thu, 04 May 2023 03:28:17 GMT  
		Size: 53.7 MB (53743996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cac1ecc551211cfcab1d45d1de16721f9d20a27ef0e52b2adf31859d333838`  
		Last Modified: Thu, 04 May 2023 03:28:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31f29f7a03315e507d400c1a1b033fc171796bca6b2d6941d6421c22c5a392`  
		Last Modified: Thu, 04 May 2023 12:07:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9381488481354093bfcb09c7b7909be364891740daf76a34a566d1f486b944b`  
		Last Modified: Thu, 04 May 2023 12:08:02 GMT  
		Size: 64.1 MB (64117634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:8759bbfb602f98591aac066a79eff8eb0ecd9e6b19cbe5152263389275b20e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:9e1e8ec7f4bb2217b1cbce86643c6f0305a7ee635d70db85b332417b9e90084e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189675179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94509c56cb2653b9ceacfe6e282b9e83b813c2aa70785c3253f7f6f1369c8af3`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 15:24:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:24 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 15:24:24 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:24 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169f9f66a850797b94faa23b04741c9d1f56ca205e1131d826b0c3195d58ef87`  
		Last Modified: Thu, 04 May 2023 15:25:54 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e00127c78968f1f0a3b074cd8a39e0deb43271df123e2e8fc09f7911c612c`  
		Last Modified: Thu, 04 May 2023 15:25:59 GMT  
		Size: 92.1 MB (92092938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a67f299f855752cfdb678b844cf72694c848bc53ba7273f0b473eddb7b396a0`  
		Last Modified: Thu, 04 May 2023 15:25:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:feae17cd40d127d9623943e9cb635f91df5679f5e57efe664636a622623a7065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181492283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0abb24452f8f7e038de90db947860eb7be2c6a02b51c0d733c155aa8cf5983`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:52:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:52:06 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:52:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:52:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 11:49:51 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 11:49:51 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 11:50:06 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:50:14 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 11:50:14 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 11:50:14 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:50:14 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 11:50:14 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 11:50:14 GMT
EXPOSE 2424
# Thu, 04 May 2023 11:50:15 GMT
EXPOSE 2480
# Thu, 04 May 2023 11:50:15 GMT
EXPOSE 8182
# Thu, 04 May 2023 11:50:15 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe39f2d222e718fa2fcf09ffc515022b8134ad2bd86f1eade8de914c8b900e5`  
		Last Modified: Thu, 04 May 2023 06:54:34 GMT  
		Size: 12.1 MB (12066173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e637393c956ae291142bb334658dcc4041571b8ec39500ad13c11acd6d4b93`  
		Last Modified: Thu, 04 May 2023 06:54:39 GMT  
		Size: 50.3 MB (50304911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a09d7f45da0bae2c893dc41b117962a9dcdbd589e6fd5caeb3e25f194c3d6d`  
		Last Modified: Thu, 04 May 2023 06:54:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ddd3684eeb7166a6af89ae4fa15d8340088348df2c3fd8feb73703b44d8ac0`  
		Last Modified: Thu, 04 May 2023 11:50:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698a438e644e7623ecd5fecd1669946ac9fc30425b478a474f56ac21965afb0`  
		Last Modified: Thu, 04 May 2023 11:50:44 GMT  
		Size: 92.1 MB (92092978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21af25c2da116312fbf9b08baf61f9f80094f3e5b509d8fe9b389b558579f12`  
		Last Modified: Thu, 04 May 2023 11:50:38 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:05efb1535865a400ed53a3a27dc844cabf400f8ce83a409ac3af385ac34aa741
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186692172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09d7366b3fa0dc120f56846cdff6b8d734aa319f6f0e24996c8cc5f4d1834dc`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 12:07:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 12:07:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 12:07:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:07:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 12:07:49 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 12:07:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:07:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 12:07:50 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 2424
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 12:07:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c1cae9037b6c50ec0e053161e5ec3654c581e3b9d0f3dd60da90f7e1af01b5`  
		Last Modified: Thu, 04 May 2023 03:28:17 GMT  
		Size: 53.7 MB (53743996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cac1ecc551211cfcab1d45d1de16721f9d20a27ef0e52b2adf31859d333838`  
		Last Modified: Thu, 04 May 2023 03:28:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e50ab11c4bbb38b693593885740f62b6863a06ac8215e3ee906b994e87775`  
		Last Modified: Thu, 04 May 2023 12:08:12 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfca2b04194cef0fa6227fc430a9df0f0785ea5878a1ca7e945919728b728be`  
		Last Modified: Thu, 04 May 2023 12:08:16 GMT  
		Size: 92.1 MB (92092986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5aa7ce54d8b8777dd7ad89ed6b8ec2b86235ca6fdd19a6feeb98d50e236471`  
		Last Modified: Thu, 04 May 2023 12:08:12 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.18`

```console
$ docker pull orientdb@sha256:015b42ff02e128806d681d304b77c2d1c277503a83a4145f2571a209fc58644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.18` - linux; amd64

```console
$ docker pull orientdb@sha256:371ca05cf3a787b97e237139828e3853ea0396ce80658e54e1281d70b964a360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161698471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec79a4d1a5bd908b7f8c80be8b60fd152581df754fbee215a9041e08e9ae4c8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 15:24:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:13 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:13 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:13 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:13 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a369a4a53bfe75f0c7a153b6ae4e9d3baa988889cc13eab8f7a9bce36d3fea`  
		Last Modified: Thu, 04 May 2023 15:25:39 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c28b9a56815881546f634776daa23f47bfacfb23ac30b5a2406eef9201df26`  
		Last Modified: Thu, 04 May 2023 15:25:43 GMT  
		Size: 64.1 MB (64117603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.18` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c96c8fd6845c6f5fa215bcdbc222ad91aadb8ad11564769cf4be22359c666fb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153515537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ad7af142600c43403751a5d07fa068013886c301a40b3eca13f0451c97cf25`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:52:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:52:06 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:52:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:52:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 11:49:51 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 11:49:51 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 11:49:55 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:49:59 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 11:49:59 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:49:59 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 11:49:59 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2424
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2480
# Thu, 04 May 2023 11:50:00 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe39f2d222e718fa2fcf09ffc515022b8134ad2bd86f1eade8de914c8b900e5`  
		Last Modified: Thu, 04 May 2023 06:54:34 GMT  
		Size: 12.1 MB (12066173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e637393c956ae291142bb334658dcc4041571b8ec39500ad13c11acd6d4b93`  
		Last Modified: Thu, 04 May 2023 06:54:39 GMT  
		Size: 50.3 MB (50304911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a09d7f45da0bae2c893dc41b117962a9dcdbd589e6fd5caeb3e25f194c3d6d`  
		Last Modified: Thu, 04 May 2023 06:54:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924586c2893e089e4558ef6681218c1d10ce60496ebe1c552da7cfe645816ebd`  
		Last Modified: Thu, 04 May 2023 11:50:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f6c35c6787ff833785be548c2bbd673122f545a6d153679668ac7ce2be587`  
		Last Modified: Thu, 04 May 2023 11:50:28 GMT  
		Size: 64.1 MB (64117612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.18` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:59b19f96d8495998a9151188f2db85e879e30466464eb699d2ea044099aae178
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158715442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfdcb2dce484053fc8078d13095615aa83779cc4923415bbff27bac733b02df`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 12:07:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 12:07:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 12:07:35 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:07:38 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 12:07:39 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:07:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 12:07:39 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2424
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2480
# Thu, 04 May 2023 12:07:39 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c1cae9037b6c50ec0e053161e5ec3654c581e3b9d0f3dd60da90f7e1af01b5`  
		Last Modified: Thu, 04 May 2023 03:28:17 GMT  
		Size: 53.7 MB (53743996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cac1ecc551211cfcab1d45d1de16721f9d20a27ef0e52b2adf31859d333838`  
		Last Modified: Thu, 04 May 2023 03:28:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31f29f7a03315e507d400c1a1b033fc171796bca6b2d6941d6421c22c5a392`  
		Last Modified: Thu, 04 May 2023 12:07:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9381488481354093bfcb09c7b7909be364891740daf76a34a566d1f486b944b`  
		Last Modified: Thu, 04 May 2023 12:08:02 GMT  
		Size: 64.1 MB (64117634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.18-tp3`

```console
$ docker pull orientdb@sha256:8759bbfb602f98591aac066a79eff8eb0ecd9e6b19cbe5152263389275b20e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.18-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:9e1e8ec7f4bb2217b1cbce86643c6f0305a7ee635d70db85b332417b9e90084e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189675179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94509c56cb2653b9ceacfe6e282b9e83b813c2aa70785c3253f7f6f1369c8af3`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 15:24:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 15:24:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:24 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 15:24:24 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:24 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:24 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169f9f66a850797b94faa23b04741c9d1f56ca205e1131d826b0c3195d58ef87`  
		Last Modified: Thu, 04 May 2023 15:25:54 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e00127c78968f1f0a3b074cd8a39e0deb43271df123e2e8fc09f7911c612c`  
		Last Modified: Thu, 04 May 2023 15:25:59 GMT  
		Size: 92.1 MB (92092938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a67f299f855752cfdb678b844cf72694c848bc53ba7273f0b473eddb7b396a0`  
		Last Modified: Thu, 04 May 2023 15:25:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.18-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:feae17cd40d127d9623943e9cb635f91df5679f5e57efe664636a622623a7065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181492283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0abb24452f8f7e038de90db947860eb7be2c6a02b51c0d733c155aa8cf5983`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:52:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:52:06 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:52:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:52:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 11:49:51 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 11:49:51 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 11:50:02 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 11:50:06 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:50:14 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 11:50:14 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 11:50:14 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:50:14 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 11:50:14 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 11:50:14 GMT
EXPOSE 2424
# Thu, 04 May 2023 11:50:15 GMT
EXPOSE 2480
# Thu, 04 May 2023 11:50:15 GMT
EXPOSE 8182
# Thu, 04 May 2023 11:50:15 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe39f2d222e718fa2fcf09ffc515022b8134ad2bd86f1eade8de914c8b900e5`  
		Last Modified: Thu, 04 May 2023 06:54:34 GMT  
		Size: 12.1 MB (12066173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e637393c956ae291142bb334658dcc4041571b8ec39500ad13c11acd6d4b93`  
		Last Modified: Thu, 04 May 2023 06:54:39 GMT  
		Size: 50.3 MB (50304911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a09d7f45da0bae2c893dc41b117962a9dcdbd589e6fd5caeb3e25f194c3d6d`  
		Last Modified: Thu, 04 May 2023 06:54:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ddd3684eeb7166a6af89ae4fa15d8340088348df2c3fd8feb73703b44d8ac0`  
		Last Modified: Thu, 04 May 2023 11:50:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698a438e644e7623ecd5fecd1669946ac9fc30425b478a474f56ac21965afb0`  
		Last Modified: Thu, 04 May 2023 11:50:44 GMT  
		Size: 92.1 MB (92092978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21af25c2da116312fbf9b08baf61f9f80094f3e5b509d8fe9b389b558579f12`  
		Last Modified: Thu, 04 May 2023 11:50:38 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.18-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:05efb1535865a400ed53a3a27dc844cabf400f8ce83a409ac3af385ac34aa741
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186692172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09d7366b3fa0dc120f56846cdff6b8d734aa319f6f0e24996c8cc5f4d1834dc`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 12:07:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 12:07:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_MD5=f92ecd2c9802938237702e3c9751c08f
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6416d714801fad65f75ac9667b91f99e5fab8ca6
# Thu, 04 May 2023 12:07:42 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.18/orientdb-tp3-3.2.18.tar.gz
# Thu, 04 May 2023 12:07:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:07:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 12:07:49 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 04 May 2023 12:07:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:07:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 12:07:50 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 2424
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 12:07:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 12:07:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c1cae9037b6c50ec0e053161e5ec3654c581e3b9d0f3dd60da90f7e1af01b5`  
		Last Modified: Thu, 04 May 2023 03:28:17 GMT  
		Size: 53.7 MB (53743996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cac1ecc551211cfcab1d45d1de16721f9d20a27ef0e52b2adf31859d333838`  
		Last Modified: Thu, 04 May 2023 03:28:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e50ab11c4bbb38b693593885740f62b6863a06ac8215e3ee906b994e87775`  
		Last Modified: Thu, 04 May 2023 12:08:12 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfca2b04194cef0fa6227fc430a9df0f0785ea5878a1ca7e945919728b728be`  
		Last Modified: Thu, 04 May 2023 12:08:16 GMT  
		Size: 92.1 MB (92092986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5aa7ce54d8b8777dd7ad89ed6b8ec2b86235ca6fdd19a6feeb98d50e236471`  
		Last Modified: Thu, 04 May 2023 12:08:12 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:015b42ff02e128806d681d304b77c2d1c277503a83a4145f2571a209fc58644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:371ca05cf3a787b97e237139828e3853ea0396ce80658e54e1281d70b964a360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161698471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec79a4d1a5bd908b7f8c80be8b60fd152581df754fbee215a9041e08e9ae4c8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 15:24:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 15:24:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:13 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:13 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:13 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:13 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a369a4a53bfe75f0c7a153b6ae4e9d3baa988889cc13eab8f7a9bce36d3fea`  
		Last Modified: Thu, 04 May 2023 15:25:39 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c28b9a56815881546f634776daa23f47bfacfb23ac30b5a2406eef9201df26`  
		Last Modified: Thu, 04 May 2023 15:25:43 GMT  
		Size: 64.1 MB (64117603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:c96c8fd6845c6f5fa215bcdbc222ad91aadb8ad11564769cf4be22359c666fb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153515537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ad7af142600c43403751a5d07fa068013886c301a40b3eca13f0451c97cf25`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:52:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:52:06 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:52:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:52:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 11:49:51 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 11:49:51 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 11:49:51 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 11:49:55 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:49:59 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 11:49:59 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:49:59 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 11:49:59 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2424
# Thu, 04 May 2023 11:50:00 GMT
EXPOSE 2480
# Thu, 04 May 2023 11:50:00 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe39f2d222e718fa2fcf09ffc515022b8134ad2bd86f1eade8de914c8b900e5`  
		Last Modified: Thu, 04 May 2023 06:54:34 GMT  
		Size: 12.1 MB (12066173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e637393c956ae291142bb334658dcc4041571b8ec39500ad13c11acd6d4b93`  
		Last Modified: Thu, 04 May 2023 06:54:39 GMT  
		Size: 50.3 MB (50304911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a09d7f45da0bae2c893dc41b117962a9dcdbd589e6fd5caeb3e25f194c3d6d`  
		Last Modified: Thu, 04 May 2023 06:54:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924586c2893e089e4558ef6681218c1d10ce60496ebe1c552da7cfe645816ebd`  
		Last Modified: Thu, 04 May 2023 11:50:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f6c35c6787ff833785be548c2bbd673122f545a6d153679668ac7ce2be587`  
		Last Modified: Thu, 04 May 2023 11:50:28 GMT  
		Size: 64.1 MB (64117612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:59b19f96d8495998a9151188f2db85e879e30466464eb699d2ea044099aae178
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158715442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfdcb2dce484053fc8078d13095615aa83779cc4923415bbff27bac733b02df`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:25:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:25:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 12:07:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 12:07:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_VERSION=3.2.18
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=ebb79d5e8f947c0d031cfaad8ce1d153
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1b1f452032092f5f3c9704b12adeb95e9b21969
# Thu, 04 May 2023 12:07:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.18/orientdb-community-3.2.18.tar.gz
# Thu, 04 May 2023 12:07:35 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 12:07:38 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 12:07:39 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 12:07:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 12:07:39 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2424
# Thu, 04 May 2023 12:07:39 GMT
EXPOSE 2480
# Thu, 04 May 2023 12:07:39 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb3595122d1cb6fffe722e2624c3c89b00776b393256a5444af56ceda691cf`  
		Last Modified: Thu, 04 May 2023 03:28:13 GMT  
		Size: 12.5 MB (12463858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c1cae9037b6c50ec0e053161e5ec3654c581e3b9d0f3dd60da90f7e1af01b5`  
		Last Modified: Thu, 04 May 2023 03:28:17 GMT  
		Size: 53.7 MB (53743996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cac1ecc551211cfcab1d45d1de16721f9d20a27ef0e52b2adf31859d333838`  
		Last Modified: Thu, 04 May 2023 03:28:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d31f29f7a03315e507d400c1a1b033fc171796bca6b2d6941d6421c22c5a392`  
		Last Modified: Thu, 04 May 2023 12:07:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9381488481354093bfcb09c7b7909be364891740daf76a34a566d1f486b944b`  
		Last Modified: Thu, 04 May 2023 12:08:02 GMT  
		Size: 64.1 MB (64117634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
