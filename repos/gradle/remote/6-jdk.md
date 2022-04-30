## `gradle:6-jdk`

```console
$ docker pull gradle@sha256:995e3c4a35be623c0ce38307c184fbb1a02d3ab92672f4bdda10cd3c978cdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:b392970e2a9daa9cefdb5a60af1e5a29a8851b0931a0b676ecc2942456d281a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414154112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da574e92a2f7dd65590d36dff24f2aac628118f4c935a4b533dfb80f4495bdb`
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
# Wed, 27 Apr 2022 18:21:44 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:21:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Apr 2022 18:21:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 18:21:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:21:59 GMT
CMD ["jshell"]
# Wed, 27 Apr 2022 18:46:54 GMT
CMD ["gradle"]
# Wed, 27 Apr 2022 18:46:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 Apr 2022 18:46:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 27 Apr 2022 18:46:54 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 Apr 2022 18:46:55 GMT
WORKDIR /home/gradle
# Wed, 27 Apr 2022 18:47:13 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 27 Apr 2022 18:48:04 GMT
ENV GRADLE_VERSION=6.9.2
# Wed, 27 Apr 2022 18:48:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Wed, 27 Apr 2022 18:48:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:7f5190524da85ee6b25c3ccb4690a1322738dd080a876971535bf57ba336d9c5`  
		Last Modified: Wed, 27 Apr 2022 18:27:00 GMT  
		Size: 192.5 MB (192474619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bc0fbc88196995c7f35050aa28ebe2028a23284a06740d2edd8eebcff4b4`  
		Last Modified: Wed, 27 Apr 2022 18:26:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001c63a4ae36bb5875e12f895eff843c005e315c38e21c762a373039287c3936`  
		Last Modified: Wed, 27 Apr 2022 18:50:17 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311a12340251f1c73943d3ab7a5cbeb3c9b4c6bd8e5557e23099e2fa1b43684e`  
		Last Modified: Wed, 27 Apr 2022 18:50:28 GMT  
		Size: 65.6 MB (65646927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643c5be27f0f495d3cbca914039b613057211c5b0f996a1e2876c8621e562455`  
		Last Modified: Wed, 27 Apr 2022 18:52:37 GMT  
		Size: 107.7 MB (107690424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; arm variant v7

```console
$ docker pull gradle@sha256:dde88660dac37a20842d00ea785fbb19b333629a8695cfd5c86ee9910c95f79b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 MB (400423906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2060ae1ace72ead0c6618db42325800b4969f9091624dba407a45405c014145`
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
# Fri, 29 Apr 2022 23:59:51 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Sat, 30 Apr 2022 00:00:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:00:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:00:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 30 Apr 2022 00:00:18 GMT
CMD ["jshell"]
# Sat, 30 Apr 2022 02:48:47 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 02:48:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 02:48:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 02:48:49 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 02:48:50 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 02:49:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 02:52:31 GMT
ENV GRADLE_VERSION=6.9.2
# Sat, 30 Apr 2022 02:52:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sat, 30 Apr 2022 02:52:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:88916e0fa83734124cf1ad963d76333eb2a10d5dbd4e50bca0be2e978056ffc5`  
		Last Modified: Sat, 30 Apr 2022 00:08:42 GMT  
		Size: 189.4 MB (189425287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4c5d2a5860390c2a6863740857031007569f582c44cc1cb66458181c7c09f3`  
		Last Modified: Sat, 30 Apr 2022 00:07:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f51b21370667dd057b58b37132c1e94ec5f7d1f4bb61fc0b3e2b544a979437`  
		Last Modified: Sat, 30 Apr 2022 02:57:49 GMT  
		Size: 4.3 KB (4349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329bd1e5e4e6e1311c13bc446ae2360a712bf97fdb0660a934abe0d9c1b2143e`  
		Last Modified: Sat, 30 Apr 2022 02:58:32 GMT  
		Size: 60.0 MB (60034480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c881ff05203c51c5c8eb707d59f70867a53ed9811ba60876a9c3cb73a003be4e`  
		Last Modified: Sat, 30 Apr 2022 03:02:32 GMT  
		Size: 107.7 MB (107690373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bba80f0b2e4a56039b998b1cc92b27ea0cd94a411e99674fcf2246a5de27d327
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (411964668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b093261a803241fcb1f8e84d963a97f5a88a58486bb4f33a5c4a503737d53480`
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
# Fri, 29 Apr 2022 23:30:47 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Fri, 29 Apr 2022 23:31:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:31:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:31:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 29 Apr 2022 23:31:10 GMT
CMD ["jshell"]
# Sat, 30 Apr 2022 02:16:55 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 02:16:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 02:16:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 02:16:58 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 02:16:59 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 02:17:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 02:18:47 GMT
ENV GRADLE_VERSION=6.9.2
# Sat, 30 Apr 2022 02:18:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sat, 30 Apr 2022 02:18:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:b7e5e8918d0d736facba8e0e27424624af1fd10901d269e27fc8b82f55acf3e9`  
		Last Modified: Fri, 29 Apr 2022 23:35:37 GMT  
		Size: 191.2 MB (191243879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5f4aeec5b0b94d80676a5e7259bf79600dfdad34ee8c179fd4b6a6b6b52ddb`  
		Last Modified: Fri, 29 Apr 2022 23:35:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed9984a1087affa2df5f617c342bbd76f933ca57ecca60a48599c2fda19b39`  
		Last Modified: Sat, 30 Apr 2022 02:21:12 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290de86cc5b0ba35adbfd2d37ab43f39a5d2e031a564806d705f08d7a8722669`  
		Last Modified: Sat, 30 Apr 2022 02:21:22 GMT  
		Size: 65.4 MB (65357252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba680b7cd759054915ff364c3acae3e761b2942c4317c972d272d84efd393f21`  
		Last Modified: Sat, 30 Apr 2022 02:23:32 GMT  
		Size: 107.7 MB (107690356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:f241b616d9478951cdc25fb0f467bad46952fa7481a03cbcc679572495d1b59c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428571756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e911e8af3aa574c6de3958525b0adfcbb96adbda11022bf6c79097a6a05e1d07`
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
# Wed, 27 Apr 2022 18:20:26 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:21:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Apr 2022 18:21:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 18:21:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:21:18 GMT
CMD ["jshell"]
# Wed, 27 Apr 2022 18:55:06 GMT
CMD ["gradle"]
# Wed, 27 Apr 2022 18:55:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 Apr 2022 18:55:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 27 Apr 2022 18:55:17 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 Apr 2022 18:55:20 GMT
WORKDIR /home/gradle
# Wed, 27 Apr 2022 18:56:54 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 27 Apr 2022 18:58:33 GMT
ENV GRADLE_VERSION=6.9.2
# Wed, 27 Apr 2022 18:58:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Wed, 27 Apr 2022 18:58:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:01b90234441b418273f6f316a4f748010fe69627fc50d61a8d49683caeeda251`  
		Last Modified: Wed, 27 Apr 2022 18:28:01 GMT  
		Size: 191.9 MB (191880523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cd45886589e9f895e2209c652eb50aa79b70dc83730e13a3a3203a41a64864`  
		Last Modified: Wed, 27 Apr 2022 18:27:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858aa50c36e81df5d6256d2f119b6302fb7483fcf161580265c63ec18d0c807b`  
		Last Modified: Wed, 27 Apr 2022 19:01:07 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd2eda97203a215aeb74e7c9251efca05d2b21f5878abad5bec6bbfd40222df`  
		Last Modified: Wed, 27 Apr 2022 19:01:22 GMT  
		Size: 74.0 MB (74015633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d54ee9a276c5918bb7c363e290d2e9c7b56a4f8f892f67896bbb0980823ba5`  
		Last Modified: Wed, 27 Apr 2022 19:03:01 GMT  
		Size: 107.7 MB (107690417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:f94a3b8750e1f68639e63689e7ac515b336da62b2896c705d9086104d9b84e5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399236753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af8614690ff05e37942612787c387468bf1c0c486c0c35d7199fe3b2e7ba01e`
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
# Fri, 29 Apr 2022 23:23:41 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Fri, 29 Apr 2022 23:23:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:23:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:23:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 29 Apr 2022 23:23:53 GMT
CMD ["jshell"]
# Sat, 30 Apr 2022 01:08:58 GMT
CMD ["gradle"]
# Sat, 30 Apr 2022 01:08:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 Apr 2022 01:08:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Sat, 30 Apr 2022 01:08:59 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 Apr 2022 01:08:59 GMT
WORKDIR /home/gradle
# Sat, 30 Apr 2022 01:09:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 30 Apr 2022 01:10:42 GMT
ENV GRADLE_VERSION=6.9.2
# Sat, 30 Apr 2022 01:10:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
# Sat, 30 Apr 2022 01:10:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8b356fd8702d5ffa2e066ed0be45a023a779bba4dd1a68fd11bc2a6bdc981e8f
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
	-	`sha256:3b842748d22e4d3654d79d4d62be80507b571087ba3e09b42c45bde81a4c0bfc`  
		Last Modified: Fri, 29 Apr 2022 23:26:06 GMT  
		Size: 180.4 MB (180404994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb17d5d583910ba96a34fa21c66dc9e92376a997213ae37b74695ef612fbde8`  
		Last Modified: Fri, 29 Apr 2022 23:25:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee12c4c8c78b5220f11d75b34f5a7270c4370af620fd4bb90a7c8d3ab7161bd`  
		Last Modified: Sat, 30 Apr 2022 01:12:37 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a67c935e0c816356d40658fcd1c44b84b54e7c273face53d0a8cf6370619aa2`  
		Last Modified: Sat, 30 Apr 2022 01:12:48 GMT  
		Size: 64.8 MB (64836175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661088fc2f9661c079e989c49324893c45b0e41f61259992ebd4306fa7d3e626`  
		Last Modified: Sat, 30 Apr 2022 01:13:58 GMT  
		Size: 107.7 MB (107690364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
