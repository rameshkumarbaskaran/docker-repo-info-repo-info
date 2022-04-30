## `gradle:jdk18`

```console
$ docker pull gradle@sha256:2d624658670c69ebc14754c54308d73b3f0d5c03ffe44c0811b5862c3bb22edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk18` - linux; amd64

```console
$ docker pull gradle@sha256:097856312db083522c9daae3ecbe1bff828ceb5bd8d92f6d893eacd03c911372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423285688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e32d0c7042a0dd14e5e015f2df92a328246a79d4c02b78e954f7ce52a45375c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:05:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:06:30 GMT
ENV JAVA_VERSION=jdk-18+36
# Fri, 22 Apr 2022 02:06:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:06:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:06:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 02:06:50 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 08:54:23 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 08:54:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 08:54:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 08:54:24 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 08:54:24 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 08:54:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 08:54:43 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 08:54:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 08:54:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eba7eb4b0706bdc82016e578b506e90d02ab8407a4ac8ed832da3eb310a8494`  
		Last Modified: Fri, 22 Apr 2022 02:09:43 GMT  
		Size: 19.8 MB (19771621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33245e75cce12da72da2411775e6cd7054f60e30ed0a50300212a23b8f4066da`  
		Last Modified: Fri, 22 Apr 2022 02:11:12 GMT  
		Size: 193.4 MB (193432343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5383940554afb16e3ae87d655848965808256d09f52eefb2883f442b78099b1e`  
		Last Modified: Fri, 22 Apr 2022 02:10:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2fe5916e96ddfe824e475a7b0f315fa62d49933b1774ef521eee9803e77a1`  
		Last Modified: Fri, 22 Apr 2022 08:58:07 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e9a229e5dce044068b399a9bab4764bbb81dcffc1bd68950ec114e972dc2a5`  
		Last Modified: Fri, 22 Apr 2022 08:58:19 GMT  
		Size: 65.6 MB (65644182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4aa6dffffb9f46d2bc22dc024721179ac9cdc23c355542f5c27aefa25c1196`  
		Last Modified: Fri, 22 Apr 2022 08:58:14 GMT  
		Size: 115.9 MB (115867025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk18` - linux; arm variant v7

```console
$ docker pull gradle@sha256:2c109408676644a9b61dac0ec445eec5fb452c7d089dc8a7974ddfcfa3cab88b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409765325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06656db5c0b6824bc3b48cda1aa9f06b3e2f675a987e3a1522e37685403ea132`
-	Default Command: `["gradle"]`

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
# Sat, 30 Apr 2022 02:50:19 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 02:50:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 02:50:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 02:50:22 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 02:50:22 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 02:51:13 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 02:51:14 GMT
ENV GRADLE_VERSION=7.4.2
# Sat, 30 Apr 2022 02:51:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Sat, 30 Apr 2022 02:51:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
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
	-	`sha256:3e9230f6ec50e7be3c8df8943941fce7b653e805b8e50d068ebfd1dfe65f10cc`  
		Last Modified: Sat, 30 Apr 2022 02:59:24 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cbdeeb8a6a02628a43b8bc23c0612178c191da98af273f86e7551b791ce68d`  
		Last Modified: Sat, 30 Apr 2022 03:00:07 GMT  
		Size: 60.0 MB (60033389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a9d72b7ff1e2548efa386003662396aa6b8150489f831f5ef1af767cb7c712`  
		Last Modified: Sat, 30 Apr 2022 02:59:57 GMT  
		Size: 115.9 MB (115867003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk18` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8c581697cc41a59f6fe156decc5924350f53990e4a3062c8a41cc761f53d3072
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 MB (421197528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c3b038680bbf500d26a6fabdeef7bd38d0392cdbcc57b6d20ff5bd6e4764b`
-	Default Command: `["gradle"]`

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
# Sat, 30 Apr 2022 02:17:39 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 02:17:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 02:17:42 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 02:17:43 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 02:18:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 02:18:06 GMT
ENV GRADLE_VERSION=7.4.2
# Sat, 30 Apr 2022 02:18:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Sat, 30 Apr 2022 02:18:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
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
	-	`sha256:8201baf53be778c4ce47ec7d72cb14bffa56679c5ea69fe3ad0220b6e33974d9`  
		Last Modified: Sat, 30 Apr 2022 02:22:09 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc713ce40b39cb532c64dd7691d96dfad08d992b5aaabf3191fe024156f94a6`  
		Last Modified: Sat, 30 Apr 2022 02:22:19 GMT  
		Size: 65.4 MB (65357408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce95d4a11155f1334be7c2e30ec66db2e2db621718a709211529211a1961972`  
		Last Modified: Sat, 30 Apr 2022 02:22:18 GMT  
		Size: 115.9 MB (115866839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk18` - linux; ppc64le

```console
$ docker pull gradle@sha256:ea102aa376b60693f99aabe8b79cdc3cd38cf3baa27e5281803325c4da544ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437701083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0abbcd12123d1a8bda84852ced5d33fa27d97a4cad971bc7620dcb5d97fd192`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 Apr 2022 08:08:14 GMT
ADD file:f1c44e93e7a6c0fb06800e11460dc680e252dff4a20297ab2eed86e559398616 in / 
# Fri, 22 Apr 2022 08:08:17 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 09:45:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 09:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:54:42 GMT
ENV JAVA_VERSION=jdk-18+36
# Fri, 22 Apr 2022 09:55:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e696d2b5995ae008b6ee7392d73ace13c36460a5e9600740c40e094079a62d28';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_aarch64_linux_hotspot_18_36.tar.gz';          ;;        armhf|arm)          ESUM='4cb2e1fe9a14a990ad0dc8f3afcd9c1b37a8d7750754c3a1e72665ef6beb300f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_arm_linux_hotspot_18_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='90790055be8147103a4a9b6a6545d42d7c5eb5616901b660c8ada68c7d067956';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_ppc64le_linux_hotspot_18_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='e711965a3c482a63d0116bcb0f3c1d06b84171c4be1995f3ac9f139d316fe149';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_s390x_linux_hotspot_18_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82d67983f92f16b5fb57176fa4c228e44ecc6f671b3c3523140fba7fb904dceb';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18%2B36/OpenJDK18U-jdk_x64_linux_hotspot_18_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 09:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 09:55:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 09:55:37 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 13:46:29 GMT
CMD ["gradle"]
# Fri, 22 Apr 2022 13:46:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Apr 2022 13:46:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 22 Apr 2022 13:46:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Apr 2022 13:46:53 GMT
WORKDIR /home/gradle
# Fri, 22 Apr 2022 13:50:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 22 Apr 2022 13:50:47 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 22 Apr 2022 13:51:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 22 Apr 2022 13:51:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:30c729c4ac9a0cf192e6c3e5618b0e930ca2ecdd73c01d9c5fed5b0707eb8836`  
		Last Modified: Tue, 19 Apr 2022 13:15:19 GMT  
		Size: 33.3 MB (33290375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b871f7e17903642296f4fb5f218d67a797860ca4d97df5f5cd9f44cc0e39ed8a`  
		Last Modified: Fri, 22 Apr 2022 10:00:23 GMT  
		Size: 21.7 MB (21690280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84676354a21f841e033b6418bb9e9df7a6e7203c3421a295bfa90212a4167c4`  
		Last Modified: Fri, 22 Apr 2022 10:02:21 GMT  
		Size: 192.8 MB (192833851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab238e6929beca9b3f9df6bc45896acc1a35dd57c7ccc7c9ee7e04a3fffa4b4`  
		Last Modified: Fri, 22 Apr 2022 10:02:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0b6c09257553038f508ecb40706cf3a61211e99ab1d2be1bb67ca685db0d47`  
		Last Modified: Fri, 22 Apr 2022 13:57:29 GMT  
		Size: 4.4 KB (4383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7fe7ec962764bd51fa427f8726e35f3e8c26ab77ba3b00eab335ef25af9d9b`  
		Last Modified: Fri, 22 Apr 2022 13:57:44 GMT  
		Size: 74.0 MB (74015088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e84c492c1c06d8ac6c579bd2af569d59ad2ff789aa7f7f2b55849a9d387771`  
		Last Modified: Fri, 22 Apr 2022 13:57:40 GMT  
		Size: 115.9 MB (115866945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk18` - linux; s390x

```console
$ docker pull gradle@sha256:5644689f2e3b99f58327cc38acc79dd50f6913c3df46b4366ec421e327ac2cb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408423503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63380057c73a99b08b9eb0c7db4c2c491b823a45a739eb3340aaceecb1563e7b`
-	Default Command: `["gradle"]`

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
# Sat, 30 Apr 2022 01:09:40 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 01:09:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 01:09:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 01:09:40 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 01:09:41 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 01:10:01 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 01:10:04 GMT
ENV GRADLE_VERSION=7.4.2
# Sat, 30 Apr 2022 01:10:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Sat, 30 Apr 2022 01:10:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
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
	-	`sha256:d16b22db8e4fcf309c8ea6c294ad5ef33d890c99bdbb66894901acb8a13c79ee`  
		Last Modified: Sat, 30 Apr 2022 01:13:17 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5c202e3529ac2ecd303e0a4488592ac7fc705c3948afba7520fa3563171df8`  
		Last Modified: Sat, 30 Apr 2022 01:13:27 GMT  
		Size: 64.8 MB (64836710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d43d343ef4bebe3a49d533ba4090aa88898b07670bb559ff49d60ffd4ecfa`  
		Last Modified: Sat, 30 Apr 2022 01:13:22 GMT  
		Size: 115.9 MB (115866999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
