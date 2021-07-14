## `adoptopenjdk:16-hotspot-focal`

```console
$ docker pull adoptopenjdk@sha256:d7ca3caaff4640d4ea9219bae9194b514a4a011c63316ab1c345cdbb54bfd070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `adoptopenjdk:16-hotspot-focal` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:7f7a96270e2233babd098394cd84b00e9a7f02bf5d792be49d6e4887509ae0aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251071150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8784c46efcab3bb2fbf2dc8a1da9051d7b3652ec887317ce0897038b54267b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:31:54 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Wed, 14 Jul 2021 00:32:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:32:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:32:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946fa19401fa4d43d4f525f700080d2aedf36159b8ab7385485a77656811aa23`  
		Last Modified: Wed, 14 Jul 2021 00:47:41 GMT  
		Size: 206.5 MB (206472211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-hotspot-focal` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:e09da021c423ea3588ad1398a4c80a5b3577f373617a25d0d3b555c74b27a915
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227692236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b58871d25f65b0076fcdd864abd567272837d956daceaca122bf18ccabc4cb4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 01:28:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 01:29:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:32:13 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Wed, 14 Jul 2021 01:32:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 01:32:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 01:32:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3374ff0390670de6a897592ab5ae9d7b16efe9170df99397d09cef4f6c91dab4`  
		Last Modified: Wed, 14 Jul 2021 01:36:42 GMT  
		Size: 14.9 MB (14899010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140ca2d7d5953ef6b47dcf2848c24df8b103579890da3889d11f044030042282`  
		Last Modified: Wed, 14 Jul 2021 01:43:55 GMT  
		Size: 188.7 MB (188731160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-hotspot-focal` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:799af62e5aee5e4bda7adca94e334e2a4156676ce50404043bcd9b594cdd23d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247157663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01910603248b5f3da35c1ffa0dc696dc123f1077f4d2342ac73b23ec2dcad664`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:20:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:20:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:22:04 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 13 Jul 2021 23:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:22:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cecec673b168a0ebad3a078ce217e36ce02c414e41ae4f1da4d174e8fdda1b`  
		Last Modified: Tue, 13 Jul 2021 23:24:23 GMT  
		Size: 15.9 MB (15894072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6f80ce8f9680625016fe0a7107fe941ab889a1440bc1cbe16a0e13b527a28b`  
		Last Modified: Tue, 13 Jul 2021 23:27:16 GMT  
		Size: 204.1 MB (204094510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-hotspot-focal` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:be914f09f6486552b8bc80400a95d2ca806e971c273bc81c3e16a80a7fdb3164
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237420694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e183affff8c9ff88d7e836c2ad1644e0063dd43d4fa74da8f7b1f8c499509763`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:36:36 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 18 Jun 2021 01:37:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:37:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:37:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1647112d6f81f9ed44c7eb5783c5c811bbd13d392ba2c6bc021ec72890de70`  
		Last Modified: Fri, 18 Jun 2021 01:55:34 GMT  
		Size: 186.9 MB (186934016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-hotspot-focal` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:c832fcc9880639f1fc46a7fc504a252867346b942aa0e5869acbe05ff08813e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222725139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24021264dcd6920d18fe894ee12b8a5f900f06afcf24ea6e760d8438bd8021a2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:20:55 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 13 Jul 2021 23:21:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:21:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:21:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1e7f6eb16ba16cfd1b897405b99b9c5f4cc0106d81f77992c222988c0784d6`  
		Last Modified: Tue, 13 Jul 2021 23:34:25 GMT  
		Size: 179.8 MB (179834126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
