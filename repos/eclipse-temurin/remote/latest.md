## `eclipse-temurin:latest`

```console
$ docker pull eclipse-temurin@sha256:f3fbf1ad599d4b5dbdd7ceb55708d10cb9fafb08e094ef91e92aa63b520a232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:latest` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:81b8481b570155419ec2b057f4a367d6f0f22a5700aa01b7de7ceaa731519b1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248522081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f546b418bb3af906a8180260ea58f79cb49c6e88e9d08b014fbd3bf4eb542093`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:45 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 02:47:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 02:47:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426329e266e460bc5ce7cd2ad6d6841e68381cc09efc53c243182eb221cce102`  
		Last Modified: Thu, 16 Mar 2023 02:54:51 GMT  
		Size: 201.1 MB (201116542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4059624ea044152b112a63a260d905e9e04009d3d4bdc57dd873c36824574d`  
		Last Modified: Thu, 16 Mar 2023 02:54:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:324ab82fa7c6f881b7468fd6ef3b006d29a63a30499c2366c4956a1ff91582a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241684101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2fc410ae3edcdcd0591042d1ba4434ff5e690fd25744bc782d51a0de4b686f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:50:35 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 02:50:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 02:50:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e662a9c01c71ac4b4b8027ff42ccad439158b083048c82ad2b060bccc493e9`  
		Last Modified: Thu, 16 Mar 2023 02:58:24 GMT  
		Size: 197.6 MB (197564751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c11f02832b62cc130402ab4fdd03a6266f71049615df803fb6eed84dfd982c2`  
		Last Modified: Thu, 16 Mar 2023 02:58:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:263d86d2b3ee21b8c6e66fa9739e72d22965389b8429e68d742593c7bdedb4cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246656351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c4407722ed272b1d5de803db3293f12ec19527cec8dbc2015cb0eb1316b9d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:53 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:56:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:56:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:56:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2729b1b1a1eb26f34be8b2488d03a6bb526c408aab70fc43ee6e4165a53205c4`  
		Last Modified: Thu, 16 Mar 2023 02:02:10 GMT  
		Size: 199.9 MB (199867833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451a95ea2c9925ad7dc6bd88a2097d789b120c2b99c2f135e5216e38f3fb1e4`  
		Last Modified: Thu, 16 Mar 2023 02:01:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bee4fb705acf9d2b2f00d1d5f6e74d7d431400cae27dd488209fd6ff27f657ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254259858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8a0c5ba7dd334dd4c4ac805737bc4ccab2f60e304416b043e0f55f7425f588`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:05:27 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 04:05:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:05:54 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:05:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c2f517e92e571b609a861a5c3adf087f14f6550d84efd77440e862bf91c1b2`  
		Last Modified: Thu, 16 Mar 2023 04:16:43 GMT  
		Size: 200.3 MB (200290291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205f512b01b6d7bbec49a117c4f677d101cb683e9bac4c2738e215b319717ce7`  
		Last Modified: Thu, 16 Mar 2023 04:16:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:027f01303822c74c4d00a21e4c54364d93d3232ba09c4d3b2874e8dcee1a9a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233911793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25ff8c3260cd963ddc92215bf34c90aa9a2bcbbace1ff5668f38dac4ca299e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:09:11 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 02:09:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:09:25 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 02:09:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783289d04781a13855572439e7ce8350076d5953968dfef42091f64340412c7d`  
		Last Modified: Thu, 16 Mar 2023 02:15:01 GMT  
		Size: 188.5 MB (188510741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b258dbf724be874ebced90e4cd5d9eb5cf77f676a8b4527ad251dfa9f3707b3e`  
		Last Modified: Thu, 16 Mar 2023 02:14:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:63eda634f5d9a815692a523839d0be579df044337ca47d611ddfba7f8f715fc9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2081191626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e9b02e13e4338923bd5267ace4c803722c47fee387016a90360efa728409ae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:16:54 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:18:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_windows_hotspot_19.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_windows_hotspot_19.0.2_7.msi ;     Write-Host ('Verifying sha256 (b2372bd728a5a708a4ce5ec6cc8b46489e5292051f4993568ec1d5f395f7e06e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b2372bd728a5a708a4ce5ec6cc8b46489e5292051f4993568ec1d5f395f7e06e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:18:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 01:18:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e880df44bcce9ac24c1802639bf4b36af2e701350626da466fa43cf0c60190`  
		Last Modified: Thu, 16 Mar 2023 01:50:41 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b558332c7adb7b7a46cff131db3681f3d69dc435e8a7226ee88531dc272020`  
		Last Modified: Thu, 16 Mar 2023 01:51:15 GMT  
		Size: 366.7 MB (366694736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc648c8f8904cf09fe4b0995cefbb44318d90754950dace4205e29f288e5558`  
		Last Modified: Thu, 16 Mar 2023 01:50:41 GMT  
		Size: 552.5 KB (552544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2158a5efd3b2b31460d8fcc7b0af31d0858438ce161c77694830b96890896c6`  
		Last Modified: Thu, 16 Mar 2023 01:50:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:89ae19b3138be4a3539d896fffd26a28d62b8827c3537a616899b7f3296bba0c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2383943457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26b6e9f274ea93d8239c77fffa4ca455a9b5764366fbf4b37f52901f8d23817`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 01:19:09 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:21:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_windows_hotspot_19.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_windows_hotspot_19.0.2_7.msi ;     Write-Host ('Verifying sha256 (b2372bd728a5a708a4ce5ec6cc8b46489e5292051f4993568ec1d5f395f7e06e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b2372bd728a5a708a4ce5ec6cc8b46489e5292051f4993568ec1d5f395f7e06e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 01:22:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Mar 2023 01:22:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25110a113aad9bb60dd17ef9518b688794c3e7e43bdbea5e2afbd4f50b40e7c4`  
		Last Modified: Thu, 16 Mar 2023 01:51:26 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a6414ff8cd6ca1872743dad9e99b0b48ce1fa5ed4ffcfc3c3a98b3300fb0f8`  
		Last Modified: Thu, 16 Mar 2023 01:52:00 GMT  
		Size: 366.5 MB (366474976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e57cea7db6938a16f16d1389f9f70b401ad0ff514b80332f41504626ad955`  
		Last Modified: Thu, 16 Mar 2023 01:51:28 GMT  
		Size: 4.0 MB (3955292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a02519efaec8f9f307ce85bb7af24fb1ce61d3bf8759ea8ac6b103fc3e37686`  
		Last Modified: Thu, 16 Mar 2023 01:51:26 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
