## `gradle:7-jdk11-jammy`

```console
$ docker pull gradle@sha256:73e242c0f915b472bb625d0e954c35b6828f6b6deb40a353f131fb5f5512eb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jdk11-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:7e54eaf339dc6f9336d251b497e58642f2152c1f58996f7126e6326d7f19e64b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.1 MB (415092567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7eb2cedf8334d48ca9101f5891dedd358cac7b3f1d512d49b9770e884f66f12`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:16:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:17:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='be07af349f0d2e1ffb7e01e1e8bac8bffd76e22f6cc1354e5b627222e3395f41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:17:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 02:17:16 GMT
CMD ["jshell"]
# Fri, 16 Jun 2023 06:48:50 GMT
CMD ["gradle"]
# Fri, 16 Jun 2023 06:48:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jun 2023 06:48:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Jun 2023 06:48:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jun 2023 06:48:50 GMT
WORKDIR /home/gradle
# Fri, 16 Jun 2023 06:49:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Jun 2023 06:50:55 GMT
ENV GRADLE_VERSION=7.6.1
# Fri, 16 Jun 2023 06:50:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
# Fri, 16 Jun 2023 06:50:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b6b86b9b9ec784135c9a4adac0cdf59f8b0812134b00402f67714b92e13d6`  
		Last Modified: Fri, 16 Jun 2023 02:20:59 GMT  
		Size: 12.5 MB (12495197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba8c6502095766c92a2e7a79a3ff9e416e6d8512f198997f09b5ef274ac2b49`  
		Last Modified: Fri, 16 Jun 2023 02:22:20 GMT  
		Size: 198.6 MB (198553540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad9c340a28e77cc641b061c97d577ba736ff5ae31e419a50575e3fddc805cb4`  
		Last Modified: Fri, 16 Jun 2023 02:22:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829569faeb0a2bd0912d05825828235ccf33567a1611f9661efcc5dd5feaadaf`  
		Last Modified: Fri, 16 Jun 2023 06:54:16 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb567ff8775fa2a8bac040be66cee2a389c43c177935400f3d0e214d0f09c9a`  
		Last Modified: Fri, 16 Jun 2023 06:54:25 GMT  
		Size: 51.5 MB (51530964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2160235bb8c7d95d4fed737825672bd86b92ae4834fefaf4e4efb9f411b8e0`  
		Last Modified: Fri, 16 Jun 2023 06:57:32 GMT  
		Size: 122.1 MB (122077290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:44a96ca610fa854472d3dedce62d43b43c21053554c330f67f90dede8a910e93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401062874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49efaa4a43826caf9cf73648050b30800ab7a2f4079c3b2c7efdbb5a2f699f73`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 01:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 01:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 01:25:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:26:42 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 01:26:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='be07af349f0d2e1ffb7e01e1e8bac8bffd76e22f6cc1354e5b627222e3395f41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 01:26:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 01:26:55 GMT
CMD ["jshell"]
# Fri, 16 Jun 2023 01:55:25 GMT
CMD ["gradle"]
# Fri, 16 Jun 2023 01:55:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jun 2023 01:55:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Jun 2023 01:55:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jun 2023 01:55:26 GMT
WORKDIR /home/gradle
# Fri, 16 Jun 2023 01:55:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Jun 2023 01:57:32 GMT
ENV GRADLE_VERSION=7.6.1
# Fri, 16 Jun 2023 01:57:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
# Fri, 16 Jun 2023 01:57:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:de11f41b5c8ee0d3b259584977df4adb3e9b005f95756baecf491f70b498f301`  
		Last Modified: Wed, 07 Jun 2023 02:07:45 GMT  
		Size: 27.0 MB (27026252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2711d7845bde07690537fe1554a2423cd444ce4ffbb31127db200abacd8bc137`  
		Last Modified: Fri, 16 Jun 2023 01:29:20 GMT  
		Size: 12.1 MB (12062599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff254c3e2465a7df4d48b67701c83ad434df1a8281189511eea6b2200f4ce3e`  
		Last Modified: Fri, 16 Jun 2023 01:30:41 GMT  
		Size: 186.0 MB (186029929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8372b49ce3f2f623d36dc49dc76bad616c5bbb581214b5edfd86614f0827bce`  
		Last Modified: Fri, 16 Jun 2023 01:30:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48e8edfd4249b8ce91edac6abfc3e6c3c514ea71d4427b5d3e6da0fba40070a`  
		Last Modified: Fri, 16 Jun 2023 02:00:48 GMT  
		Size: 4.4 KB (4354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdce9c05e8bf3f82cfb0def5f16c4d3f81cced3bd55edacc9950bf10171a4b`  
		Last Modified: Fri, 16 Jun 2023 02:00:57 GMT  
		Size: 53.9 MB (53862295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187ef7ca78825caf54702f0be490a425a2d3d2b7523567ed6d38c12e35dcd5b2`  
		Last Modified: Fri, 16 Jun 2023 02:04:07 GMT  
		Size: 122.1 MB (122077270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2454d2510083f0425f323e5b73ba6c2a0d95ad5c4625bdf29ad5549e03db4d4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.4 MB (409365299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98669ae1fd3a06b05a51d21ceade546ace789ab3239b368503e125cefc110f5d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:46:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:46:41 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:46:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='be07af349f0d2e1ffb7e01e1e8bac8bffd76e22f6cc1354e5b627222e3395f41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:46:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 02:46:54 GMT
CMD ["jshell"]
# Fri, 16 Jun 2023 05:02:22 GMT
CMD ["gradle"]
# Fri, 16 Jun 2023 05:02:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jun 2023 05:02:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Jun 2023 05:02:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jun 2023 05:02:23 GMT
WORKDIR /home/gradle
# Fri, 16 Jun 2023 05:02:36 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Jun 2023 05:04:07 GMT
ENV GRADLE_VERSION=7.6.1
# Fri, 16 Jun 2023 05:04:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
# Fri, 16 Jun 2023 05:04:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a707fe2fc3c87da15576bd7b678fe8f2591ad481cc638b8cfe52664b47d2cf`  
		Last Modified: Fri, 16 Jun 2023 02:49:56 GMT  
		Size: 12.5 MB (12454449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679c26e1cd19f0dfc7dbe5439226d7dcc3c98f3b86d45f9f6690bcc8f5692452`  
		Last Modified: Fri, 16 Jun 2023 02:51:07 GMT  
		Size: 195.3 MB (195331064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c30826cf61339c60583be702571399b45cb14352609fce277058693ae0e352e`  
		Last Modified: Fri, 16 Jun 2023 02:50:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2303d951f60f6913db330be5692864ecd66b7b7e39adb0b91893cdc31488506`  
		Last Modified: Fri, 16 Jun 2023 05:07:04 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2b5a8d90f15d5e97de51da7fffaa80371a954bffc0c0d14ce8840ae75b061`  
		Last Modified: Fri, 16 Jun 2023 05:07:11 GMT  
		Size: 51.1 MB (51108735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c3879332224a4c95ab13f79148ae577f6c1e4f9bc8d003fde53660dc9a6c25`  
		Last Modified: Fri, 16 Jun 2023 05:10:08 GMT  
		Size: 122.1 MB (122077306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:63e27e607a757a7e964a642c868081f9991d91b95213d7caa01d6420411ac209
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.4 MB (407437773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de799af1c63be0a0ead9aa0b8544da7daa831cdf3b8a70a5de8ef0a2308646f2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:19:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 16 Jun 2023 02:21:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='be07af349f0d2e1ffb7e01e1e8bac8bffd76e22f6cc1354e5b627222e3395f41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:22:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 02:22:02 GMT
CMD ["jshell"]
# Fri, 16 Jun 2023 07:04:56 GMT
CMD ["gradle"]
# Fri, 16 Jun 2023 07:04:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jun 2023 07:05:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 16 Jun 2023 07:05:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jun 2023 07:05:02 GMT
WORKDIR /home/gradle
# Fri, 16 Jun 2023 07:06:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 16 Jun 2023 07:15:38 GMT
ENV GRADLE_VERSION=7.6.1
# Fri, 16 Jun 2023 07:15:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
# Fri, 16 Jun 2023 07:15:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3d88337241ae7be52d0828f504ae3cf9cb25b0e583dee0724bdab39614aefd`  
		Last Modified: Fri, 16 Jun 2023 02:26:58 GMT  
		Size: 13.3 MB (13317562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3241cb1bb27b27aac37378104bc58935dced5fd966591de92753c7c1bec271`  
		Last Modified: Fri, 16 Jun 2023 02:28:48 GMT  
		Size: 180.5 MB (180539585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03534fe54ad509da372aa0112f6b2d782f1b906cad1a8be43d72b4a8d8494b69`  
		Last Modified: Fri, 16 Jun 2023 02:28:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3f44b62d0f585df5df16b80c7c4683df6997449134765eb1d321f99f7759b6`  
		Last Modified: Fri, 16 Jun 2023 07:21:40 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492ba7511720bb63230bb3523847f448fce0fc923ae12fa938e33184f9da6f72`  
		Last Modified: Fri, 16 Jun 2023 07:21:55 GMT  
		Size: 55.8 MB (55787458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba6695d4b0caeb68d7da9f512790949cc0b1784e8a93037e044840109ded8e0`  
		Last Modified: Fri, 16 Jun 2023 07:25:56 GMT  
		Size: 122.1 MB (122077230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:ec0a2620954d44a5ae47b51b6ae0a40ef0b585b5479025535f69756ae982c77f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 MB (386528476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e3828b1c467f1e429076f9e7fffe4fa8e90f3c4ba838d62ba7629e86e9020`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:33:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:33:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:33:37 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 01 Jun 2023 23:33:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='be07af349f0d2e1ffb7e01e1e8bac8bffd76e22f6cc1354e5b627222e3395f41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:33:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 01 Jun 2023 23:33:52 GMT
CMD ["jshell"]
# Fri, 02 Jun 2023 15:34:16 GMT
CMD ["gradle"]
# Fri, 02 Jun 2023 15:34:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jun 2023 15:34:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Jun 2023 15:34:17 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jun 2023 15:34:17 GMT
WORKDIR /home/gradle
# Fri, 02 Jun 2023 15:34:39 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Jun 2023 15:35:36 GMT
ENV GRADLE_VERSION=7.6.1
# Fri, 02 Jun 2023 15:35:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
# Fri, 02 Jun 2023 15:35:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6147605a23b4eff6c334927a86ff3508cb5d6722cd624c97ded4c2e8640f1f87
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f2957179c3a13374d05630725d1d996f8083efadf7d2da999c9b4ca53ab7c98f`  
		Last Modified: Thu, 01 Jun 2023 23:19:06 GMT  
		Size: 28.6 MB (28648005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24acb432e66acb8b18b12789af1090ed1e30afb01008c2e9f116021dee19ba1a`  
		Last Modified: Thu, 01 Jun 2023 23:35:59 GMT  
		Size: 12.5 MB (12546367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732c2e6225f66189e7e83ad7c4c9c5bc30f4d135ead957a7424b966b70ff6722`  
		Last Modified: Thu, 01 Jun 2023 23:36:08 GMT  
		Size: 172.0 MB (171995815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf9b3f1ce96d0ac98c8e6515568d6fe0e2d95480048f101ffee6bcee060e2de`  
		Last Modified: Thu, 01 Jun 2023 23:35:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94ea70c9cf96282cedef2782bc0d6409dc41bbe1f1314bf3c82718d9edece38`  
		Last Modified: Fri, 02 Jun 2023 15:37:33 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f2258de9c59d94ae9ecc62c1a0e94ff3e4db0723fd634103825d492dfa22a2`  
		Last Modified: Fri, 02 Jun 2023 15:37:41 GMT  
		Size: 51.3 MB (51256480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807ab70f2f7e3b72cb9b474cd04eff5585b8fb65eb4f671eecef9a757f9551f3`  
		Last Modified: Fri, 02 Jun 2023 15:38:38 GMT  
		Size: 122.1 MB (122077269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
