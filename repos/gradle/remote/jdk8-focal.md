## `gradle:jdk8-focal`

```console
$ docker pull gradle@sha256:02c4a5f155c4b55e7eac5f4ecc4f7e9abb8d572cb4a9898f66a4d26904502770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:155e0261739f829874a2c730c045bfc676b151893219197b012e3f9e58da1aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289558198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad37a8f61cc86602a97d5e1240b646a66c836254da7214090295d72efaf620`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:19:51 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Wed, 26 Apr 2023 19:19:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 26 Apr 2023 19:19:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 26 Apr 2023 20:41:03 GMT
CMD ["gradle"]
# Wed, 26 Apr 2023 20:41:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Apr 2023 20:41:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Apr 2023 20:41:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Apr 2023 20:41:03 GMT
WORKDIR /home/gradle
# Wed, 26 Apr 2023 20:41:31 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Apr 2023 20:41:31 GMT
ENV GRADLE_VERSION=8.1.1
# Wed, 26 Apr 2023 20:41:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
# Wed, 26 Apr 2023 20:41:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9057c0404ad9792542034fcff11993972d3371debf9897e1ba5c900d15edde0b`  
		Last Modified: Wed, 26 Apr 2023 19:26:52 GMT  
		Size: 54.6 MB (54646245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460b4ae467f85d83b56e87b8cf4aabcc9baf3705378bbd72e7a2161580fd3d16`  
		Last Modified: Wed, 26 Apr 2023 19:26:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f36469198a5a45b49d68941f65be8cd78dcf929dd09f1fd11f2fdf60bc25a6`  
		Last Modified: Wed, 26 Apr 2023 20:48:26 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28810eaaa06749ca8a795df38fee2b8bc1d49946d8f1c1f226154d514569672a`  
		Last Modified: Wed, 26 Apr 2023 20:48:36 GMT  
		Size: 65.3 MB (65308983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759da9f00790ade8023b16ba373323aac3bae55b8576573f167c0dd7e1abbe40`  
		Last Modified: Wed, 26 Apr 2023 20:48:32 GMT  
		Size: 124.7 MB (124672876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:5147c3e5bb1e36a29d19dc61ef320c532ff2e807a59ceeb5b205663d0b1d2063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274461580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eef15ababd7814b4b6eac61bbb5c0bde00d5ca0dc7ddbc7cb0a151482d9f179`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:27 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 18 Apr 2023 01:52:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 18 Apr 2023 01:52:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 18 Apr 2023 02:46:05 GMT
CMD ["gradle"]
# Tue, 18 Apr 2023 02:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Apr 2023 02:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 18 Apr 2023 02:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Apr 2023 02:46:05 GMT
WORKDIR /home/gradle
# Tue, 18 Apr 2023 02:46:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 22 Apr 2023 00:57:29 GMT
ENV GRADLE_VERSION=8.1.1
# Sat, 22 Apr 2023 00:57:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
# Sat, 22 Apr 2023 00:57:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4f91de5e7255da1ddca4bca0d16197240bc77687db29597c7379aada3f33a`  
		Last Modified: Tue, 18 Apr 2023 01:54:32 GMT  
		Size: 50.3 MB (50297013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99667012d2f08614c1498ebf1e4ad4e0cadfa90d8a0b9262d97c30ad5649bf7`  
		Last Modified: Tue, 18 Apr 2023 01:54:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feaf54da0b72b471421227b05068fa4cf18c41b2d7ce106a72ff2edc7d7cf7b`  
		Last Modified: Tue, 18 Apr 2023 02:49:28 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e131d98c78f80d2b06af4061a0df5cfa561e80178321b8446e4ef7185dc700e`  
		Last Modified: Tue, 18 Apr 2023 02:49:38 GMT  
		Size: 59.7 MB (59722514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4846c34aaa2365a70df8929dca9f620c080c4a9ceda7f7138572bc6f1d5e7f`  
		Last Modified: Sat, 22 Apr 2023 00:59:48 GMT  
		Size: 124.7 MB (124672902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9af4563a3124150eadf507ca8a0354ed13374372cda71f89d070219586588c94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287067409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87876575b7a162a6e57cd30dd9036c327b5c88eb4ccfb5a7597583e7ce0cd54`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:39:26 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 10:38:10 GMT
CMD ["gradle"]
# Thu, 04 May 2023 10:38:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 May 2023 10:38:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 04 May 2023 10:38:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 May 2023 10:38:11 GMT
WORKDIR /home/gradle
# Thu, 04 May 2023 10:38:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 04 May 2023 10:38:43 GMT
ENV GRADLE_VERSION=8.1.1
# Thu, 04 May 2023 10:38:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
# Thu, 04 May 2023 10:38:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8458dca1b69ff01ddfa6c98929321ceeb6d3de1a5cada07c5852a4086d7a3e94`  
		Last Modified: Thu, 04 May 2023 03:28:02 GMT  
		Size: 53.7 MB (53744559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a79ca23fd90b52cbfec617108c84cb5c00523ffb346e570c9e43e8160308a5e`  
		Last Modified: Thu, 04 May 2023 03:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97424601efd9d6361024c34ac1eab404e02da57e03e40ce3d4c0b8bd1e0d90`  
		Last Modified: Thu, 04 May 2023 10:41:44 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa54331dc8a48a96fbe3d19c8c490d2a4b62bfad7ccf7e6f59ab07ce37abb64`  
		Last Modified: Thu, 04 May 2023 10:41:53 GMT  
		Size: 65.2 MB (65235640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98ca0083565b0fb3bc68401c892256769bb072e06ef5fd9ffcf9fc56f8c93fa`  
		Last Modified: Thu, 04 May 2023 10:41:50 GMT  
		Size: 124.7 MB (124672938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:e8dd3195c72bdb7b230a1f3a97b23ea5dc5886596babae7f4b241f7a23517116
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301429415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66da1602924875743d4cd07ced7a46e53b3b9603c2acbece6492330284a1c497`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:16:37 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Wed, 26 Apr 2023 19:16:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 26 Apr 2023 19:16:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 26 Apr 2023 20:03:31 GMT
CMD ["gradle"]
# Wed, 26 Apr 2023 20:03:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Apr 2023 20:03:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Apr 2023 20:03:34 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Apr 2023 20:03:35 GMT
WORKDIR /home/gradle
# Wed, 26 Apr 2023 20:04:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Apr 2023 20:04:44 GMT
ENV GRADLE_VERSION=8.1.1
# Wed, 26 Apr 2023 20:04:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
# Wed, 26 Apr 2023 20:04:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e111cb9948407e26351227dabce49822fb88c37ee72f1d1582a69c68af2e702f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e96798d84a73841888c112a029a5898d26bd508606efddb9044bf3d665c5e6`  
		Last Modified: Wed, 26 Apr 2023 19:27:57 GMT  
		Size: 52.1 MB (52134545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70715a91cc235dd410342c2f2253a3e11051cf02082ead99297517362181f91c`  
		Last Modified: Wed, 26 Apr 2023 19:27:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac72845c4422247579b3671d9aeab91dfbabd7210d1726817e3c32c82166b0a3`  
		Last Modified: Wed, 26 Apr 2023 20:14:56 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae629e9d6ffecaa010d9accf22431566cba296392820d6933e1a435ff9431f`  
		Last Modified: Wed, 26 Apr 2023 20:15:17 GMT  
		Size: 73.7 MB (73733956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6393f111921f70b0e6cd5095dc7648ecd34f5598c87dd7f61ff7a2adfa6a0e`  
		Last Modified: Wed, 26 Apr 2023 20:15:07 GMT  
		Size: 124.7 MB (124672877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
