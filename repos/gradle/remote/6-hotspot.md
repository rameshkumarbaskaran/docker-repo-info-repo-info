## `gradle:6-hotspot`

```console
$ docker pull gradle@sha256:bf3f80422fc330b5a40b3a5497d61326a43c4283dcdc019c95e78b73f2113703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6-hotspot` - linux; amd64

```console
$ docker pull gradle@sha256:fb8a5638f13106d3b5dd8d1c104bc9ba1a5f44bef0144ee4764d60838052ff1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321918020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a612261e0ec9d35190db0b0dd7be42e2d400836485fdadee341734a89db774d1`
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
# Fri, 18 Jun 2021 00:29:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:29:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jul 2021 17:30:10 GMT
CMD ["gradle"]
# Fri, 02 Jul 2021 17:30:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jul 2021 17:30:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 02 Jul 2021 17:30:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jul 2021 17:30:12 GMT
WORKDIR /home/gradle
# Fri, 02 Jul 2021 17:31:11 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 17:37:05 GMT
ENV GRADLE_VERSION=6.9
# Fri, 02 Jul 2021 17:37:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Fri, 02 Jul 2021 17:37:10 GMT
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
	-	`sha256:1fff23190c570a076a1de98fb808bfb1c3de3bfcb3c0bf5dddb9b221dd2aabb8`  
		Last Modified: Fri, 18 Jun 2021 00:39:36 GMT  
		Size: 103.6 MB (103551845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177842773b7f25528627646e699a5499abf7eb163e7c2c3c4ea8742281fae0c4`  
		Last Modified: Fri, 02 Jul 2021 17:41:04 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d38405d3c2e751422f4a2839650f862bcb2735228aa429c59e48129dccca469`  
		Last Modified: Fri, 02 Jul 2021 17:41:20 GMT  
		Size: 65.6 MB (65625891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa92d3090af7025bd7f7681fc2792d804a06d342c337bda7c6fa5be5c498fae`  
		Last Modified: Fri, 02 Jul 2021 17:50:16 GMT  
		Size: 108.1 MB (108149194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-hotspot` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fd3800472eee21fac27dcbf4baaa9715a7b4e2e8c7a8339361b11d4b23c2527a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319492481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61180afd49fd1b8b515306cd024be3c955ef7294a8a390906c9c60fec733a9c5`
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
# Fri, 18 Jun 2021 00:31:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:31:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jul 2021 17:53:54 GMT
CMD ["gradle"]
# Fri, 02 Jul 2021 17:53:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jul 2021 17:53:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 02 Jul 2021 17:53:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jul 2021 17:53:55 GMT
WORKDIR /home/gradle
# Fri, 02 Jul 2021 17:54:17 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 17:58:59 GMT
ENV GRADLE_VERSION=6.9
# Fri, 02 Jul 2021 17:58:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Fri, 02 Jul 2021 17:59:03 GMT
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
	-	`sha256:c57e4be204d097505feac6ad8282ba6ec2de4d61afc4b8fac1d52940ff443b99`  
		Last Modified: Fri, 18 Jun 2021 00:35:20 GMT  
		Size: 103.0 MB (102955968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28affd41eb0af88ffbb983618d1b0fee39b9a50280dc7139ba58c5094d34bea`  
		Last Modified: Fri, 02 Jul 2021 18:05:59 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941b907af533bec1a776840caa0f59bbd09e28c6726d7aece80e8f5007b5ff86`  
		Last Modified: Fri, 02 Jul 2021 18:06:12 GMT  
		Size: 65.3 MB (65329987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8af665b7584ec717d273d6649cd439dc66cfdb7f4ff7a88fe3a80ebb28d680`  
		Last Modified: Fri, 02 Jul 2021 18:15:50 GMT  
		Size: 108.1 MB (108149186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-hotspot` - linux; ppc64le

```console
$ docker pull gradle@sha256:8d67126713b6d20e9688ec2bcac5e408e3af51eff0586e8a8df59de8013f37bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333688991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7388c7ef8f305e7f602bd9d47bc07047f729a4d8dabbf6408f61adf7c553c2`
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
# Fri, 18 Jun 2021 01:32:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:32:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 04:16:21 GMT
CMD ["gradle"]
# Thu, 08 Jul 2021 04:16:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 08 Jul 2021 04:16:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 08 Jul 2021 04:16:46 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 08 Jul 2021 04:16:52 GMT
WORKDIR /home/gradle
# Thu, 08 Jul 2021 04:20:20 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 08 Jul 2021 05:17:39 GMT
ENV GRADLE_VERSION=6.9
# Thu, 08 Jul 2021 05:17:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Thu, 08 Jul 2021 05:18:51 GMT
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
	-	`sha256:6df0819c06322e4c2f20bae71cd0bbed7197821b89e6432844441ca5dd6b08bd`  
		Last Modified: Fri, 18 Jun 2021 01:52:54 GMT  
		Size: 101.0 MB (101047884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d40354f9283e4fd1da60107761cede0db82b337a44966cb311b077efae2317`  
		Last Modified: Thu, 08 Jul 2021 05:36:15 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1923fbe45d49d1878b21fdd2144b6fef998ed5b8bfba37f002ec274f9dd109`  
		Last Modified: Thu, 08 Jul 2021 05:36:31 GMT  
		Size: 74.0 MB (74000852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd1edca2503cab49114ed51ef45a418851ecf41f1654ed33682d6fdddc45f9e`  
		Last Modified: Thu, 08 Jul 2021 05:47:33 GMT  
		Size: 108.1 MB (108149207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-hotspot` - linux; s390x

```console
$ docker pull gradle@sha256:7d39d9e40c988692e222afd4ee0e09728da7852307cd22b7e21d3ccb702a2a0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314510495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f257d11f77c5cdbd8f22fedbbe7c744e2eeea137d2afdfd6bde91a6cb34406d2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jun 2021 23:44:00 GMT
ADD file:737a08bab262cc2abc326912fdb8c8038222b272a5967b25ec6c761539c9d456 in / 
# Thu, 17 Jun 2021 23:44:02 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:09:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 00:09:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:09:42 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 18 Jun 2021 00:09:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 00:09:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jul 2021 18:06:22 GMT
CMD ["gradle"]
# Fri, 02 Jul 2021 18:06:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Jul 2021 18:06:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 02 Jul 2021 18:06:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Jul 2021 18:06:27 GMT
WORKDIR /home/gradle
# Fri, 02 Jul 2021 18:07:18 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jul 2021 18:26:16 GMT
ENV GRADLE_VERSION=6.9
# Fri, 02 Jul 2021 18:26:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
# Fri, 02 Jul 2021 18:26:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=765442b8069c6bee2ea70713861c027587591c6b1df2c857a23361512560894e
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:be436b7e641e3737311249dadcc71ad61ba7bc9597248f426c58c8548cff8af0`  
		Last Modified: Thu, 17 Jun 2021 23:45:32 GMT  
		Size: 27.1 MB (27140902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92cd82b21097d2899d125e539a498d2f79c992bd6ebee596f4d3a3fc26dd7b6`  
		Last Modified: Fri, 18 Jun 2021 00:20:59 GMT  
		Size: 15.7 MB (15741691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719fc67c12be3900eb1fcf03340fd0ff18b4c409fbdcc5e444b3319c72cfe894`  
		Last Modified: Fri, 18 Jun 2021 00:21:05 GMT  
		Size: 98.6 MB (98640868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2908a2eb63764799e9187d2c7fef7c9bef7a63e754fe99e6a65422fe571557c3`  
		Last Modified: Fri, 02 Jul 2021 18:36:54 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c32e2b7c8bb923905ae55b1ee71357baaaa87991e8f018bcb54c1d2ef4807`  
		Last Modified: Fri, 02 Jul 2021 18:37:02 GMT  
		Size: 64.8 MB (64833486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6bd3226b10e4c672d625a2456ad9c158eb839eaa3228727cbd84726a0de791`  
		Last Modified: Fri, 02 Jul 2021 19:26:55 GMT  
		Size: 108.1 MB (108149184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
