## `gradle:jdk17-jammy`

```console
$ docker pull gradle@sha256:31884c0123496be3f3f5c072347e9efe987d7233f5a9b605dd21b5c46c11cb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk17-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:48a6faaf198f069a9cd838b30780d5b830fbe696d3c588c1ad2d6542a9ac91af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372523637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35684d2126bef120507f3e7575691ba5b675de49481c799f8ebf4f296fe51aa3`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:36:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:21:08 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:21:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:21:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:21:18 GMT
CMD ["jshell"]
# Tue, 25 Jul 2023 23:50:03 GMT
CMD ["gradle"]
# Tue, 25 Jul 2023 23:50:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 25 Jul 2023 23:50:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 25 Jul 2023 23:50:04 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 25 Jul 2023 23:50:04 GMT
WORKDIR /home/gradle
# Tue, 25 Jul 2023 23:50:30 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 25 Jul 2023 23:50:31 GMT
ENV GRADLE_VERSION=8.2.1
# Tue, 25 Jul 2023 23:50:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Tue, 25 Jul 2023 23:50:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b566cb887b5c06e04f5cd97660a99e73bd52ceb9d72c6db6383ae8470cc4cf`  
		Last Modified: Tue, 04 Jul 2023 20:41:38 GMT  
		Size: 17.0 MB (17040993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2699dbfb6757dd554b60d2cc9d5e0cb7174bb7f3ce1576afd84d592b2feb3163`  
		Last Modified: Tue, 25 Jul 2023 22:26:45 GMT  
		Size: 144.8 MB (144780009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab1613eab38c1d68e665acd7d686f07f83bfc58e7b84a1af188a9dfdab4cb6`  
		Last Modified: Tue, 25 Jul 2023 22:26:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec561a0119cfaf7131fae7bd99dc80fd8e50b830e9e761590821ba479f046b`  
		Last Modified: Tue, 25 Jul 2023 23:54:30 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a93e1063aa28de420e0deaa0547a5eefc34a27b557e06974697b79f180cfad5`  
		Last Modified: Tue, 25 Jul 2023 23:54:39 GMT  
		Size: 51.5 MB (51539787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e187b65e2435fd2c02dc1c83d1683c4dc112f5b3af5614c97bc53f178d07f1cd`  
		Last Modified: Tue, 25 Jul 2023 23:54:36 GMT  
		Size: 128.7 MB (128727074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk17-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:798ced46045e594a8384b949ff09a1eed837b62400a77c723b6269d15f12a03a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369304193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b939d6848ba92016846947effcc3ecb1ad8a5c1e6142285b703d024c321ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:41:15 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:41:18 GMT
ADD file:c13f43a31510c7a4eaa7e4ca90e4f973b19895658b1f9993cab5f93979d4e2dc in / 
# Wed, 28 Jun 2023 08:41:18 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:09:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:09:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:09:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:01:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:01:27 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:01:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:01:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:01:40 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 19:01:40 GMT
CMD ["jshell"]
# Tue, 08 Aug 2023 19:39:50 GMT
CMD ["gradle"]
# Tue, 08 Aug 2023 19:39:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 08 Aug 2023 19:39:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 08 Aug 2023 19:39:51 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 08 Aug 2023 19:39:51 GMT
WORKDIR /home/gradle
# Tue, 08 Aug 2023 19:40:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 08 Aug 2023 19:40:07 GMT
ENV GRADLE_VERSION=8.2.1
# Tue, 08 Aug 2023 19:40:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Tue, 08 Aug 2023 19:40:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:63b96265cfe95b9cec847027033d4226b783ecd042036f5c809a7386027f56b0`  
		Last Modified: Fri, 30 Jun 2023 02:08:02 GMT  
		Size: 27.0 MB (27026961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fa46b0671072c68047e10f8c7e3ffe9a06840284e9e91967baa3a634b82942`  
		Last Modified: Tue, 08 Aug 2023 19:05:31 GMT  
		Size: 17.6 MB (17587022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3078180219256d703ecdfd617ff36f918648d8f12ad5bae8b652b3af60cc131`  
		Last Modified: Tue, 08 Aug 2023 19:05:41 GMT  
		Size: 142.1 MB (142062908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc7441add5c2f10628837f414b7ff7c510318cd831edbc6d4b46dfcd26c60b`  
		Last Modified: Tue, 08 Aug 2023 19:05:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2757a037dceb852282237436b682c94861c44ef977b42f483a5944628327b5`  
		Last Modified: Tue, 08 Aug 2023 19:05:27 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f4005d877b9f39fad50364172e7c0c8efbd23ab823a4f6572b7767f0898593`  
		Last Modified: Tue, 08 Aug 2023 19:45:23 GMT  
		Size: 4.4 KB (4351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd47e78c55b1e6f9a4004d6af63a7167fc10888c80332917b48501f0aa8b9e97`  
		Last Modified: Tue, 08 Aug 2023 19:45:33 GMT  
		Size: 53.9 MB (53895038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2335370ef33f3f462483fb38224d3143abac9d92613622a827c146a226f23d9`  
		Last Modified: Tue, 08 Aug 2023 19:45:37 GMT  
		Size: 128.7 MB (128727072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk17-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:75e32b28bb7c7507424038734d78f3412ed9eef2a2398b6e4e8497fc6e3937f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370252042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a79e730332a1e30ad054d73e4e9d4df665d06862db8d3f7f7673e65d8353aa6`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:34:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:26:19 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:26:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 25 Jul 2023 22:26:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:26:28 GMT
CMD ["jshell"]
# Wed, 26 Jul 2023 00:13:44 GMT
CMD ["gradle"]
# Wed, 26 Jul 2023 00:13:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 26 Jul 2023 00:13:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 26 Jul 2023 00:13:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 26 Jul 2023 00:13:45 GMT
WORKDIR /home/gradle
# Wed, 26 Jul 2023 00:14:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 26 Jul 2023 00:14:17 GMT
ENV GRADLE_VERSION=8.2.1
# Wed, 26 Jul 2023 00:14:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Wed, 26 Jul 2023 00:14:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f85d89e7da0f3af0f527e7300cced784d0ba64249b8c376690599d313cb056`  
		Last Modified: Tue, 04 Jul 2023 15:39:09 GMT  
		Size: 18.5 MB (18466568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e608d89acd4174d72876f150d75f207520b32c1cd818e9b2a961bd359ea076b`  
		Last Modified: Tue, 25 Jul 2023 22:29:19 GMT  
		Size: 143.6 MB (143550624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326c8d2e60825d8ee1f0d2cee3312be25dba2879f7678ce08547315204788d4f`  
		Last Modified: Tue, 25 Jul 2023 22:29:10 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfe956caf9ec82a913fb4f88344147302c42db6a05532ab7b76e0f76134916f`  
		Last Modified: Wed, 26 Jul 2023 00:17:02 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643175aad02e1e9f900f55390c05f759fb35716f95bd63796e089f872c834334`  
		Last Modified: Wed, 26 Jul 2023 00:17:09 GMT  
		Size: 51.1 MB (51112224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156f034637d3689617d34ccee6d1a18a69e68d5317d49640eedb7cef9c5bc47c`  
		Last Modified: Wed, 26 Jul 2023 00:17:08 GMT  
		Size: 128.7 MB (128727069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk17-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:e4d40170f014be09e34abfcd96b0fbc4884cf7e39f61c2bb5a837a887824a2c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383474477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcf69d3b8eed14b9367eae66b52a688c0d2fd74e6d0cce64379fe3a4e8c75a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 00:18:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 00:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 00:18:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:25:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:25:11 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:25:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:25:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:25:44 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 19:25:45 GMT
CMD ["jshell"]
# Tue, 08 Aug 2023 20:05:42 GMT
CMD ["gradle"]
# Tue, 08 Aug 2023 20:05:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 08 Aug 2023 20:05:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 08 Aug 2023 20:05:45 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 08 Aug 2023 20:05:46 GMT
WORKDIR /home/gradle
# Tue, 08 Aug 2023 20:06:36 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 08 Aug 2023 20:06:39 GMT
ENV GRADLE_VERSION=8.2.1
# Tue, 08 Aug 2023 20:06:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Tue, 08 Aug 2023 20:06:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db77a9bc80a636be0a061681aa78957c506eea6993305fe871da82fd4a2d8e5`  
		Last Modified: Tue, 08 Aug 2023 19:34:25 GMT  
		Size: 18.7 MB (18729537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00b21ba4b7ccf4c8d754834fb925176401e6f1f1876cdf9fbdf8909d5df0ee8`  
		Last Modified: Tue, 08 Aug 2023 19:34:40 GMT  
		Size: 144.5 MB (144495251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944e54e9f108e41f0a3f3ad458c6a06ab5fb9632a28ef0f7996f3b7efb6ccf2a`  
		Last Modified: Tue, 08 Aug 2023 19:34:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a17eb7d15d936134be780fa02e1f0b096ab5ef59b28d1ee0931193d95446f3b`  
		Last Modified: Tue, 08 Aug 2023 19:34:19 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d45244f8cf5dae8e4c8bcfad367c9f0487a1d120087053601a0fc64303048f5`  
		Last Modified: Tue, 08 Aug 2023 20:18:48 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d3d4f1631f450caf071fd222d678fc06a67a63ba105fd7b773081ff14c046f`  
		Last Modified: Tue, 08 Aug 2023 20:19:04 GMT  
		Size: 55.8 MB (55806013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed0ab9a46abd4dfe7ed9875a87dfe9ae35615ae9b6fc467b8c5293ddd02cb94`  
		Last Modified: Tue, 08 Aug 2023 20:19:00 GMT  
		Size: 128.7 MB (128726999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk17-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:fd494efb68b3cb6769b29ed049b57fae9593b10158cfa2a9c5712f572daea799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360139402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d0d47ffbdeab32f0a0792e554fa23cdf9b8ffe78bd4dcd037ce1a589e14f08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:24:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 16:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:24:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:44:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:44:32 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:44:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c43688163cfdcb1a6e6fe202cc06a51891df746b954c55dbd01430e7d7326d00';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='33d972efd78b70a07aed793a6ebcb52a5129707e8c62268e478d1c2df15898e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='88f5d14cc84a4bcfe50aa275092ae97a0edf7205269ed12c1972bf613bc52b1e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='055d8bd0eebf137cf3506fb84817ce2d858597f21067d9a1268f08916738b435';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa5fc7d388fe544e5d85902e68399d5299e931f9b280d358a3cbee218d6017b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:44:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:44:43 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:44:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 19:44:43 GMT
CMD ["jshell"]
# Tue, 08 Aug 2023 20:24:18 GMT
CMD ["gradle"]
# Tue, 08 Aug 2023 20:24:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 08 Aug 2023 20:24:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 08 Aug 2023 20:24:19 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 08 Aug 2023 20:24:19 GMT
WORKDIR /home/gradle
# Tue, 08 Aug 2023 20:24:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 08 Aug 2023 20:24:37 GMT
ENV GRADLE_VERSION=8.2.1
# Tue, 08 Aug 2023 20:24:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Tue, 08 Aug 2023 20:24:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc3ca72e7c73374cf85ad35ee727d2bb1efa34f74596d738251b2541906c7b`  
		Last Modified: Tue, 08 Aug 2023 19:47:44 GMT  
		Size: 17.3 MB (17255716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f34f82b850a04e9f2186bf9a81591ee20a9eb6ecebe86f9b4895b21a6c011e3`  
		Last Modified: Tue, 08 Aug 2023 19:47:53 GMT  
		Size: 134.2 MB (134215725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574a29079ae63de3c89369f48ebacabafaa24d12c321f650bddf6410a7b4281`  
		Last Modified: Tue, 08 Aug 2023 19:47:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb805a3d173f16204a560ba6a818b1346fe633b3d4afedf773857eb4962d938`  
		Last Modified: Tue, 08 Aug 2023 19:47:42 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411d5e98384cbd1ce9bdee669cac3c540ff71ac3e02e054ecbae02e2f8bedb0`  
		Last Modified: Tue, 08 Aug 2023 20:29:20 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7d0aed429911cce75ca4b932fb314ea57e8bcfe577c077419e0aee3ab7541`  
		Last Modified: Tue, 08 Aug 2023 20:29:28 GMT  
		Size: 51.3 MB (51289986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64d1c0b501e2ec3c94a7d6aa3b298ff1f729a55392ba7f7044b9c65ff980a4e`  
		Last Modified: Tue, 08 Aug 2023 20:29:28 GMT  
		Size: 128.7 MB (128727074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
