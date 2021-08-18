## `gradle:6-jre8-hotspot`

```console
$ docker pull gradle@sha256:d06da0df4ee63c4bf02890e3833bd8f00c7d1de5e2ac21d010638ffaaf94d6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6-jre8-hotspot` - linux; amd64

```console
$ docker pull gradle@sha256:0a213151fc003436ccf097e7432d820f5e246f350bf052be9cc8014c9e19c505
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260075904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5639de5218c0d8d187b094949768e07677b3519f2cbd91a6a58fc53874cfdbd3`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:28:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:29:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:24 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 18 Jun 2021 00:29:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:41 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jul 2021 17:31:25 GMT
CMD ["gradle"]
# Fri, 02 Jul 2021 17:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jul 2021 17:31:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 02 Jul 2021 17:31:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jul 2021 17:31:27 GMT
WORKDIR /home/gradle
# Fri, 02 Jul 2021 17:31:47 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 17:37:17 GMT
ENV GRADLE_VERSION=6.9
# Fri, 02 Jul 2021 17:37:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Fri, 02 Jul 2021 17:37:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7766c75e8fade5c21578ec8566d2929e7238f9ac1dbe88551bf2f147b76c65`  
		Last Modified: Fri, 18 Jun 2021 00:39:29 GMT  
		Size: 16.0 MB (16033037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e80a3d8823a612034fb6f6e66daff2a6ef94bcd79876803d4d5b4f5d6268a4e`  
		Last Modified: Fri, 18 Jun 2021 00:40:00 GMT  
		Size: 41.7 MB (41709463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d13d9853166bee5cfa40255883af53d3b1075d70bd48edf81b8f636bc9d1ec`  
		Last Modified: Fri, 02 Jul 2021 17:42:33 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f267be378026780de03e38ba72e330df7ee685d8ce2bd192470132d5e8851bd`  
		Last Modified: Fri, 02 Jul 2021 17:42:48 GMT  
		Size: 65.6 MB (65626159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88687703e8a84424dfbfab7a7f1971e378fc47f6613ecb6318fe3ef7e1273e10`  
		Last Modified: Fri, 02 Jul 2021 17:51:18 GMT  
		Size: 108.1 MB (108149193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jre8-hotspot` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:eaaa688c70af8fd52a3633fa1cced7d618a0057b477978aeb8377ad60463d96f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257564864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4cc65316bd56fa103fe9306e2c082bf1425a27db07567792421c616fe4bacd`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:31:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:32 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 18 Jun 2021 00:31:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:31:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jul 2021 17:54:40 GMT
CMD ["gradle"]
# Fri, 02 Jul 2021 17:54:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jul 2021 17:54:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 02 Jul 2021 17:54:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jul 2021 17:54:42 GMT
WORKDIR /home/gradle
# Fri, 02 Jul 2021 17:55:02 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 17:59:18 GMT
ENV GRADLE_VERSION=6.9
# Fri, 02 Jul 2021 17:59:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Fri, 02 Jul 2021 17:59:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff470c6007f78550376884f4972cc5c767c6adc6f7d6002adddbddfb4600ea4b`  
		Last Modified: Fri, 18 Jun 2021 00:35:11 GMT  
		Size: 15.9 MB (15894169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d45ccd7e4b335030b7765a1d0ce081c0efb5829f207c9fade226a677f59903`  
		Last Modified: Fri, 18 Jun 2021 00:35:41 GMT  
		Size: 41.0 MB (41028441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd23b3da50680b4e8db59ead57259a774dc3cf3c22f49e9cd337f693b993edcc`  
		Last Modified: Fri, 02 Jul 2021 18:07:42 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9035b9252fde72a218da0441d7eafa183395faa42e007351148b7575b035fb`  
		Last Modified: Fri, 02 Jul 2021 18:07:54 GMT  
		Size: 65.3 MB (65329903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25903f822883c467f1b06fc5351f8346bc2c4a3037141bdfbeb49375d77b30a9`  
		Last Modified: Fri, 02 Jul 2021 18:17:07 GMT  
		Size: 108.1 MB (108149187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jre8-hotspot` - linux; ppc64le

```console
$ docker pull gradle@sha256:46e098d0b196f643771303ec0126e1ac3768541643b83c1a4addb03a52a94ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273743959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343c372a44406cf71d507328791b40ebe01a22ede713011298839e9ab4fcb14b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:31:58 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 18 Jun 2021 01:32:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:33:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 04:22:05 GMT
CMD ["gradle"]
# Thu, 08 Jul 2021 04:22:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 08 Jul 2021 04:22:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 08 Jul 2021 04:22:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 08 Jul 2021 04:22:41 GMT
WORKDIR /home/gradle
# Thu, 08 Jul 2021 04:24:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 08 Jul 2021 05:19:19 GMT
ENV GRADLE_VERSION=6.9
# Thu, 08 Jul 2021 05:19:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Thu, 08 Jul 2021 05:20:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
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
	-	`sha256:4030a4fbe37b7149ec659c371a608f0b8206b81a947990cba025699072c716cf`  
		Last Modified: Fri, 18 Jun 2021 01:53:12 GMT  
		Size: 41.1 MB (41102849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c91de5e9faab7fa4ffa0a318f6f04cedf0e505d2ed723325cfbcb8ca524486`  
		Last Modified: Thu, 08 Jul 2021 05:38:04 GMT  
		Size: 4.4 KB (4389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e54dd15028456fefac3348b1cc1ae1336c16b62d68b0e072bcac62aabeca8e`  
		Last Modified: Thu, 08 Jul 2021 05:38:20 GMT  
		Size: 74.0 MB (74000814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670f48e61081a5dff84a861ed6dd3d63cbe0eba42dcec854b374284ac446c805`  
		Last Modified: Thu, 08 Jul 2021 05:48:54 GMT  
		Size: 108.1 MB (108149229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jre8-hotspot` - linux; s390x

```console
$ docker pull gradle@sha256:fc8cbe5ae8d7de4f9b3a15145a3b85419908935ab51294b050946c98f5aecd97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254718522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b453503e2c35114dc517569fafc86d0f56ebf975ddbc8dc5932a0e62c81e7d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:19:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 21:19:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:19:46 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Mon, 26 Jul 2021 21:20:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 21:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 14:44:09 GMT
CMD ["gradle"]
# Wed, 18 Aug 2021 14:44:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Aug 2021 14:44:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 18 Aug 2021 14:44:12 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Aug 2021 14:44:13 GMT
WORKDIR /home/gradle
# Wed, 18 Aug 2021 14:45:07 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 14:57:47 GMT
ENV GRADLE_VERSION=6.9
# Wed, 18 Aug 2021 14:57:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Wed, 18 Aug 2021 14:58:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2859ea56dafeb61512cbd72a03b7e2b1e762e9a60e7ca4d0bda5d8d7433dc6e`  
		Last Modified: Mon, 26 Jul 2021 21:32:13 GMT  
		Size: 15.7 MB (15741671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832a028185c560dd03389659c4fb74d4cef41ebe481f44b8c6f030e3a949bc8`  
		Last Modified: Mon, 26 Jul 2021 21:32:33 GMT  
		Size: 38.8 MB (38839471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ee1631af18a63664b0b1613634ec85bcb779be63f7d233697cfb85c8199de9`  
		Last Modified: Wed, 18 Aug 2021 15:07:28 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbac2b326cfc6c6900051f34f82afc46d98fcf44dfc08f17b45570b0dace3e6a`  
		Last Modified: Wed, 18 Aug 2021 15:07:39 GMT  
		Size: 64.8 MB (64833913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c24e84f2ec2896156e92e5d8c5233f2fed11c9f1c8e4c0f07b6e40e7fdae35e`  
		Last Modified: Wed, 18 Aug 2021 15:14:40 GMT  
		Size: 108.1 MB (108149200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
