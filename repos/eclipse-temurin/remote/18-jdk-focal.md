## `eclipse-temurin:18-jdk-focal`

```console
$ docker pull eclipse-temurin@sha256:bddf9e3bb8ee752b7a3f561ddd0e6f4bc90df8190854f21c3373efe94dcaa73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:18-jdk-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2e38313a0c68f59e4610e4b7dffe9c102c721d73801b8eaf7a1cce2da310a3d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241770740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825f0e4fc209134600cf081e4e55aa07057224d399853fd520572ded8bef89b8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:24:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:24:48 GMT
ENV JAVA_VERSION=jdk-18+36
# Sat, 30 Apr 2022 00:25:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:25:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 30 Apr 2022 00:25:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dc755b592da4b1124b1e234ecb462608d017290110a0193b350cec9a521e55`  
		Last Modified: Sat, 30 Apr 2022 00:27:40 GMT  
		Size: 19.8 MB (19772006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfb1fb4cbd521ea8fbdb2ece9138e7d1fb5c4288d10366821a25228f29bb6af`  
		Last Modified: Sat, 30 Apr 2022 00:28:38 GMT  
		Size: 193.4 MB (193432344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d960b012eb8ecbd47d4ddcc58d8994269a7535759c00098c47cda4e3392ff1f3`  
		Last Modified: Sat, 30 Apr 2022 00:28:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:9d061ec094b533b129fdee5135e98f09bec8213eef816d381c42f4f562445bd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233860584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80af6e17b972ae907daaee26aef06170f4e48b83bcd52e9ee466245238d099ee`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:56:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:59:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:00:58 GMT
ENV JAVA_VERSION=jdk-18+36
# Sat, 30 Apr 2022 00:01:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:01:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:01:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 30 Apr 2022 00:01:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362c401df4a70d7113d00849e1040eba62e153171d43aeb505cdfe041e13b30f`  
		Last Modified: Sat, 30 Apr 2022 00:07:40 GMT  
		Size: 19.2 MB (19195606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c55469cbdca8962541a7197d645897d8671bde1cd57834d88698b6d3baf7c8`  
		Last Modified: Sat, 30 Apr 2022 00:10:51 GMT  
		Size: 190.6 MB (190591168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53786a055d98c72f2c2a4f95e1cbfc3ab48efefe7874114e0e08011ad1149a`  
		Last Modified: Sat, 30 Apr 2022 00:09:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5c384447631f8bf3bb53cdcf6150483c2059bf74c7e1b328a8369434eb34896e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239968969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b69182faf15865c0f502597c9479224bb2060b4df9960bc8e51d8209b40124c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:28:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:30:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:31:40 GMT
ENV JAVA_VERSION=jdk-18+36
# Fri, 29 Apr 2022 23:31:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:31:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:31:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 29 Apr 2022 23:31:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b467f4b58f0fff42ab91803fe1a7c56675eed1a58f67991e9e7b0e445b91c1`  
		Last Modified: Fri, 29 Apr 2022 23:35:19 GMT  
		Size: 20.5 MB (20499354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a402fc50caa18dd54616de2d8887d0ddfcb2a6b725894ed6c23004fa8e2090c`  
		Last Modified: Fri, 29 Apr 2022 23:36:31 GMT  
		Size: 192.3 MB (192300100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1669e88c182480f86f71b94030c98b89ecb67fff97df739978d617044e04fb76`  
		Last Modified: Fri, 29 Apr 2022 23:36:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ce1971d5a591e261d23aac8b7df58a3d4d71bacf6abdf84a44898261528f367d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247817256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc9398307fa9455e51c76349cc8853af7c04894d842cf57e31eaabbb51a3303`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:28 GMT
ADD file:55691ac7d76af0fcfafc39ebd1e5a4f2d7018147d6db6f89812db33fbaffc2f9 in / 
# Fri, 29 Apr 2022 23:22:33 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:39:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:14 GMT
ENV JAVA_VERSION=jdk-18+36
# Sat, 30 Apr 2022 00:42:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:42:41 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:42:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 30 Apr 2022 00:43:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9c0a77cb9f0f7330e3fc62254e4c8ae89ed4bba21209fdc1088195250f950b9`  
		Last Modified: Fri, 29 Apr 2022 23:25:23 GMT  
		Size: 33.3 MB (33290661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78469566e7f98d05da9b7bb014ec6ce7170e52dbf51ed022fc29dbb9212a0e38`  
		Last Modified: Sat, 30 Apr 2022 00:47:36 GMT  
		Size: 21.7 MB (21692524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dff379c77681d1563d6c1841b51abcf84b4f0ce744ddc5589f8e61d9db9f369`  
		Last Modified: Sat, 30 Apr 2022 00:48:55 GMT  
		Size: 192.8 MB (192833909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610d5c5c042843e18646eb9e1f145b2cfa5408e76e8807dc5bb0abdd4baced78`  
		Last Modified: Sat, 30 Apr 2022 00:48:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:62eac17e76b9b9cae833b6b7d866cfc2be4b48f3dd545445fc8da8b7bc03f951
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227715429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2f04c83eb2c2a4cfe63759ed018c3ecd53f6016075608a82a1c2125999a063`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 22:50:05 GMT
ADD file:fdc1835c7f7eae641bd78a4c938c3d94746b95a0c151498d332a2b9878fd99d8 in / 
# Fri, 29 Apr 2022 22:50:07 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:23:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:24:15 GMT
ENV JAVA_VERSION=jdk-18+36
# Fri, 29 Apr 2022 23:24:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:24:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 29 Apr 2022 23:24:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e0f1090807e81093e3637ffe3d350f58816de907201055908c3506a30c68993`  
		Last Modified: Fri, 29 Apr 2022 22:52:01 GMT  
		Size: 27.1 MB (27065417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8061a8e3bb73503261725cfaf9256d8c5dc9ee8d357d1e40a4d6578ad8263162`  
		Last Modified: Fri, 29 Apr 2022 23:25:57 GMT  
		Size: 19.2 MB (19235277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6572443b8538e0a9a1f0b0e0ac60444b6815b2638a4ca8b84ee050be6dfcf47`  
		Last Modified: Fri, 29 Apr 2022 23:26:37 GMT  
		Size: 181.4 MB (181414575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14a0671a04e774b17a66cf2ab9bec123aa25c0d01707d71c472e448fc16c7c7`  
		Last Modified: Fri, 29 Apr 2022 23:26:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
