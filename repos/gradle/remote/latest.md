## `gradle:latest`

```console
$ docker pull gradle@sha256:ebfc36c3a213248618e75b1b99df5a4d1d125b7f9fd463c1fe6dc438f343e945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:latest` - linux; amd64

```console
$ docker pull gradle@sha256:39b5b96f82b805810f9032b48d11451753d68d494a9faba473a72351fc5287ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421299233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f640c96ac7466984091ea77d8180ffbcc5ae76a549ba66ed829c3542c322cf6e`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:45:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:21:12 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:21:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:21:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:21:24 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 19:42:46 GMT
CMD ["gradle"]
# Fri, 05 Nov 2021 19:42:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 05 Nov 2021 19:42:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 05 Nov 2021 19:42:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 05 Nov 2021 19:42:48 GMT
WORKDIR /home/gradle
# Fri, 05 Nov 2021 19:43:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 05 Nov 2021 19:43:09 GMT
ENV GRADLE_VERSION=7.2
# Fri, 05 Nov 2021 19:43:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 05 Nov 2021 19:43:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1fba688e4817fa2b044e9fc220607825d6d823866f99050e9f3321efdfa28d`  
		Last Modified: Sat, 16 Oct 2021 02:48:44 GMT  
		Size: 19.8 MB (19776863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3df373e15f054e24e0d95fa17206269e55fba11786b331b7b714252967596b`  
		Last Modified: Fri, 05 Nov 2021 19:25:26 GMT  
		Size: 192.9 MB (192948668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0264cf7a54d1c1d5f04aea163d6217e75a85afa86c618ce8f2668c622c5743`  
		Last Modified: Fri, 05 Nov 2021 19:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea036f7c4eea3d9416c2047d96daf83f83093cf5c4303360271af96268964fa`  
		Last Modified: Fri, 05 Nov 2021 19:45:33 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfffd9dacf31f6c748025a3cc77dab313b59641ce2f9e4a950f05e1ec3b4bac`  
		Last Modified: Fri, 05 Nov 2021 19:45:44 GMT  
		Size: 65.6 MB (65628320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502defa2027c57e53c8122350015b6d1fdfcc0ef9cbc4dce592937337a5eef04`  
		Last Modified: Fri, 05 Nov 2021 19:45:39 GMT  
		Size: 114.4 MB (114373755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; arm variant v7

```console
$ docker pull gradle@sha256:88a8dc02a3648b52dce69afff61a91faec1d168742dfdffa657fb1cbefb2fe37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407649221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be940ceec809be665925993b4a85ea3e44afc19087a1da4c49919564f29ffd72`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:41:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 18:59:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:00:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:00:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:00:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:00:17 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 20:46:56 GMT
CMD ["gradle"]
# Fri, 05 Nov 2021 20:46:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 05 Nov 2021 20:46:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 05 Nov 2021 20:46:58 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 05 Nov 2021 20:46:59 GMT
WORKDIR /home/gradle
# Fri, 05 Nov 2021 20:47:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 05 Nov 2021 20:47:51 GMT
ENV GRADLE_VERSION=7.2
# Fri, 05 Nov 2021 20:47:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 05 Nov 2021 20:48:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73092bd78be324813f4a4bdc7c75343bcc4753cf3a97145d91d7c8d8ae1ec9e`  
		Last Modified: Sat, 16 Oct 2021 02:47:09 GMT  
		Size: 19.2 MB (19196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5ca3812ed21fcbc8f27c1c9bad8ad703bea957d7656151319326fbe03b130`  
		Last Modified: Fri, 05 Nov 2021 19:06:06 GMT  
		Size: 190.0 MB (189974985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0477169fff55c8b2f84b205c0339e6a962cde1e454925b5e859a3aa07a28639`  
		Last Modified: Fri, 05 Nov 2021 19:04:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bce985bde8088d3659ab35f6c571540110d9a5f89ad068872762b6afb21917`  
		Last Modified: Fri, 05 Nov 2021 20:53:13 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5622c06cbeb0768a45ab8fbdd8fe87530fdaf06deaececdca7fc9901ce0230`  
		Last Modified: Fri, 05 Nov 2021 20:53:55 GMT  
		Size: 60.0 MB (60034986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc03a8da33ab90b2874b79717ffb65f211f2afe3fc2d85c5238a72b273b1ab`  
		Last Modified: Fri, 05 Nov 2021 20:53:45 GMT  
		Size: 114.4 MB (114373844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e9e90cc97b29423dda5a2ff5ed7787a31ab7f43660bd83993a880e33e1504c7b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.2 MB (417247840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a5ff64bc133a786ba47d9209aee93e88a86b93d9f62bf92400c6f426ed42d0`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 03:28:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:41:17 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:41:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:41:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:41:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:41:30 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 21:05:01 GMT
CMD ["gradle"]
# Fri, 05 Nov 2021 21:05:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 05 Nov 2021 21:05:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 05 Nov 2021 21:05:04 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 05 Nov 2021 21:05:05 GMT
WORKDIR /home/gradle
# Fri, 05 Nov 2021 21:05:30 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 05 Nov 2021 21:05:31 GMT
ENV GRADLE_VERSION=7.2
# Fri, 05 Nov 2021 21:05:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 05 Nov 2021 21:05:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d246d72cf3fa2492fcec79d12e7ddff4b26bc404f31671d0b6b45956f4659e21`  
		Last Modified: Sat, 16 Oct 2021 03:34:39 GMT  
		Size: 20.5 MB (20497588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c62fe607b6fbf978dd8aaefc8e820909f5b0e2e258a1f46ebcc1ce0db722d48`  
		Last Modified: Fri, 05 Nov 2021 19:45:38 GMT  
		Size: 189.9 MB (189863235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f1465365f2502f4fd118d1a6f7d79cf1f35b46c55815e828aedb5905afac59`  
		Last Modified: Fri, 05 Nov 2021 19:45:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cf4dc219f1c74758b787ad996bc633d41b4493b93a9b5ebea183ceeca9657b`  
		Last Modified: Fri, 05 Nov 2021 21:07:53 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcca2f69053100264e7927213d8c83b725c76de0e0f4b0840e690c05880f381`  
		Last Modified: Fri, 05 Nov 2021 21:08:05 GMT  
		Size: 65.3 MB (65338120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f256fae1034641b9e124acc8b0c63fcdad66e91807ba08824e02b39a98ad0cd6`  
		Last Modified: Fri, 05 Nov 2021 21:08:00 GMT  
		Size: 114.4 MB (114373554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; ppc64le

```console
$ docker pull gradle@sha256:b0611860f085cdae9a27d8df32a03b80d271ceffce925841c287064b7eba94f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.9 MB (431908176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a454989ae211dc7ff892738ff13a52c598326f49faa5f8b0b115da6415503a`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:00:40 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 01:01:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 01:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 01:01:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 01:01:22 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 03:03:48 GMT
CMD ["gradle"]
# Sat, 16 Oct 2021 03:04:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Nov 2021 01:38:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 02 Nov 2021 01:38:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Nov 2021 01:38:28 GMT
WORKDIR /home/gradle
# Tue, 02 Nov 2021 01:40:49 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 02 Nov 2021 01:40:59 GMT
ENV GRADLE_VERSION=7.2
# Tue, 02 Nov 2021 01:41:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Tue, 02 Nov 2021 01:41:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c039cd0909346123aad04b02731eff4b76a8183bac5eb82e2d477f9e3ecd1260`  
		Last Modified: Sat, 16 Oct 2021 01:05:05 GMT  
		Size: 21.7 MB (21691370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfd2de7d19685e6fa2fd563f642aee9263750b7eb94c5192fdbab6ded0ce3c9`  
		Last Modified: Sat, 16 Oct 2021 01:06:02 GMT  
		Size: 188.6 MB (188550881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c694d366736b5f652319c576193e51d7f7b576fb0a76cb475d3c252f808f2183`  
		Last Modified: Sat, 16 Oct 2021 01:05:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb64ab4c86407960598867418dc590fbb3926eab003350b00e3ce58558f14097`  
		Last Modified: Tue, 02 Nov 2021 01:46:10 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea140ce536cb5696f744123305ea28468387fab0c58ba3d306be27d20dac8400`  
		Last Modified: Tue, 02 Nov 2021 01:46:25 GMT  
		Size: 74.0 MB (74000307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3116b4dc1c15164581a9e9633e0f48c798daab443f17813bb74b559c20fb240d`  
		Last Modified: Tue, 02 Nov 2021 01:46:22 GMT  
		Size: 114.4 MB (114373849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; s390x

```console
$ docker pull gradle@sha256:94b198104f0f8e4909cce1101ee7c9ed8d0cc69e04bd0b0a630326352a15079c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.9 MB (405934772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eade17ba6377bd6004b7719fc1b76512a98c42107fbe6e6367cbf807e9b4ff`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:41:48 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:41:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:42:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:42:03 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 20:16:04 GMT
CMD ["gradle"]
# Fri, 05 Nov 2021 20:16:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 05 Nov 2021 20:16:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 05 Nov 2021 20:16:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 05 Nov 2021 20:16:05 GMT
WORKDIR /home/gradle
# Fri, 05 Nov 2021 20:16:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 05 Nov 2021 20:16:26 GMT
ENV GRADLE_VERSION=7.2
# Fri, 05 Nov 2021 20:16:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 05 Nov 2021 20:16:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d62f01df0df55e65f1037a428195076b6423d10d10ef3ae844e054d6a82597a`  
		Last Modified: Sat, 16 Oct 2021 01:01:35 GMT  
		Size: 19.2 MB (19236649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f67bf6b3f189ec83683427932c226f1aaf749d054122b356911a116386c3d21`  
		Last Modified: Fri, 05 Nov 2021 19:43:21 GMT  
		Size: 180.4 MB (180365428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956023a06e5d3dcf52d3d70db75ac254e5901921c10a51620866d519476d00`  
		Last Modified: Fri, 05 Nov 2021 19:43:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27881dec49dcdbaca9db03b8eccb891b80e25d23f7aae3c97e87d945555fdb83`  
		Last Modified: Fri, 05 Nov 2021 20:18:02 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66a66ce7799ebecec65e151f530655e371c86ec03a0eb943580ee91412ed61d`  
		Last Modified: Fri, 05 Nov 2021 20:18:12 GMT  
		Size: 64.8 MB (64833469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e6a2a16e46a4fab163f35af8c09d768628658fa95ab13612e535cabe53fd05`  
		Last Modified: Fri, 05 Nov 2021 20:18:07 GMT  
		Size: 114.4 MB (114373839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
