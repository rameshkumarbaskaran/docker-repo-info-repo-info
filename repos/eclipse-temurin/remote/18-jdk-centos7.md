## `eclipse-temurin:18-jdk-centos7`

```console
$ docker pull eclipse-temurin@sha256:f8b85d0d21d64dc06eca00765bc9d43223c6cde15986a64a8b6f2d40d39de851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:18-jdk-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ea65276c7243d63b93f6abcc5eb664b68f94d4e82ece0e2945e11657d03ad216
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282237839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2ffbc690cc6ec5f4f6b8dd786fdf1ac92f898d504de9f94dd7470d8ad65ae0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:53:12 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Thu, 31 Mar 2022 02:21:20 GMT
ENV JAVA_VERSION=jdk-18+36
# Thu, 31 Mar 2022 02:21:33 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Mar 2022 02:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Mar 2022 02:21:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Mar 2022 02:21:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eafaeccaf7b18df74301fade3ec58483f58947f3a10bbc458aa7fe6e063d060`  
		Last Modified: Wed, 15 Sep 2021 18:55:36 GMT  
		Size: 12.7 MB (12704282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36846f140faa189c928aab1126e98eba3b30239e96233f1183027f4bdc954cd2`  
		Last Modified: Thu, 31 Mar 2022 02:23:49 GMT  
		Size: 193.4 MB (193436240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99af3907138296c71c41980aed315fe8d768ad4f16b4e49362be290bf6efaf0`  
		Last Modified: Thu, 31 Mar 2022 02:23:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1a7266cea45070ce1c1bac2bb1fe041d8764f7e974a63493039c6de3d77702e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318723064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09df4d764ff429239882cb874cc61e3fd77c85ac5030280d8886a1ed1ac780e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 14 Feb 2022 19:59:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Feb 2022 20:01:29 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Wed, 30 Mar 2022 21:09:01 GMT
ENV JAVA_VERSION=jdk-18+36
# Wed, 30 Mar 2022 21:09:20 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 30 Mar 2022 21:09:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 21:09:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 30 Mar 2022 21:09:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd0ac8e8fe7aee16a10c67c8c9c7b02a8102e7dd0f11573c3265a4f6803004`  
		Last Modified: Mon, 14 Feb 2022 20:06:08 GMT  
		Size: 18.0 MB (18047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed2ed3e71a4c503719741433da5e71fec995245d1530f682eb7777341ad519`  
		Last Modified: Wed, 30 Mar 2022 21:12:32 GMT  
		Size: 192.3 MB (192300404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cdaba68af3247b73a6a5bc1f50fa9b9f138e3d227046901cdfbef59ab8a90`  
		Last Modified: Wed, 30 Mar 2022 21:12:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jdk-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:62bc3720f86fc043e9aae9700c3a2fb2dd2c641d084439b5684d3d5784bcc267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285959689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e663e93199473c9192b20ccf4a66287aa7bd7cd5024ab3770799f07ba0168463`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 21:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 21:36:04 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Thu, 31 Mar 2022 02:37:15 GMT
ENV JAVA_VERSION=jdk-18+36
# Thu, 31 Mar 2022 02:37:49 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Mar 2022 02:37:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Mar 2022 02:38:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Mar 2022 02:38:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed260bc2980920873032cc009bd67c8970c26ed48ba8792638376638344fd14`  
		Last Modified: Wed, 15 Sep 2021 21:40:23 GMT  
		Size: 12.6 MB (12607997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492dc3189006c1d99e788d35f5bbc3cab0a3527c3bc59271f05933e3ec172021`  
		Last Modified: Thu, 31 Mar 2022 02:42:00 GMT  
		Size: 192.8 MB (192835072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316a7fd72696ef4bcff12b32ca2d5dac113fc18127e8c0ef48d56a3f518d98fb`  
		Last Modified: Thu, 31 Mar 2022 02:41:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
