## `groovy:jdk16`

```console
$ docker pull groovy@sha256:b4dd04df807b79d57ab4f3c0e6390b4db800aebb56ed2dab6d38a60a4166c36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `groovy:jdk16` - linux; amd64

```console
$ docker pull groovy@sha256:05140c263410e5e93180004c93290e97d09f368b8d63941333a74aab0cee8452
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299338212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ec91baa83ec1348de0a106b1edf21bd4ea85b2a1794ad20dcf1e8f8af9528`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:26:35 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 01 Oct 2021 03:26:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:26:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:26:47 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:32:13 GMT
CMD ["groovysh"]
# Fri, 01 Oct 2021 08:32:13 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 01 Oct 2021 08:32:14 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Fri, 01 Oct 2021 08:32:14 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 01 Oct 2021 08:32:14 GMT
WORKDIR /home/groovy
# Fri, 01 Oct 2021 08:32:20 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 01 Oct 2021 08:32:20 GMT
ENV GROOVY_VERSION=3.0.9
# Fri, 01 Oct 2021 08:32:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Fri, 01 Oct 2021 08:32:40 GMT
USER groovy
# Fri, 01 Oct 2021 08:32:42 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66893017ee66c84eb5e4d032e9035f9daba47395e649ed423f2d1ee47bed3d26`  
		Last Modified: Fri, 01 Oct 2021 03:38:09 GMT  
		Size: 206.5 MB (206472212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaba15288a4cef3f2fe429d3aaf46ced2912c45380068a649bd827f52b982cf`  
		Last Modified: Fri, 01 Oct 2021 08:37:30 GMT  
		Size: 4.4 KB (4390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddbe599e9edc1bc6b7c96aff4816f4f3b166ebc038f441a0c5bb1881b63f951`  
		Last Modified: Fri, 01 Oct 2021 08:37:31 GMT  
		Size: 4.2 MB (4151429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091322086d592b3340b68a0244dc255e95d88536f7129f36410db5942948ac6`  
		Last Modified: Fri, 01 Oct 2021 08:37:34 GMT  
		Size: 44.1 MB (44107119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaeb2670324980267e24655f95bedfb28818457cf4dc8594947964cd0f17a4d`  
		Last Modified: Fri, 01 Oct 2021 08:37:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk16` - linux; arm variant v7

```console
$ docker pull groovy@sha256:cea238a8898b2bb473cf666c712dd418ec87c8d0877824e77f9f6d8eb590c6ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275392690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acff92b026a20c8956ce6bbb505e978b326043c6d1ebc178055eb630c48370ce`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:52 GMT
ADD file:f9dcf17ef0f45719dff5ed961907d78a1ea6671fecdb434536f3fc8cf15fbb3b in / 
# Tue, 31 Aug 2021 01:40:53 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:51:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:52:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:55:27 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 31 Aug 2021 02:55:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:55:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 02:55:52 GMT
CMD ["jshell"]
# Tue, 31 Aug 2021 05:46:44 GMT
CMD ["groovysh"]
# Tue, 31 Aug 2021 05:46:44 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 31 Aug 2021 05:46:46 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Tue, 31 Aug 2021 05:46:46 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 31 Aug 2021 05:46:47 GMT
WORKDIR /home/groovy
# Tue, 31 Aug 2021 05:47:00 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:05:50 GMT
ENV GROOVY_VERSION=3.0.9
# Tue, 07 Sep 2021 21:06:00 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Tue, 07 Sep 2021 21:06:01 GMT
USER groovy
# Tue, 07 Sep 2021 21:06:06 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:cccc98128e2b3db00394b4e59c3f674a52e4b861786d9fab388357a88fc428a2`  
		Last Modified: Tue, 31 Aug 2021 01:44:57 GMT  
		Size: 24.1 MB (24068823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b915f774c910de28b940b41c37fc76946eb150ac0a4048d2d2cbc5b3b0983c26`  
		Last Modified: Tue, 31 Aug 2021 02:59:59 GMT  
		Size: 14.9 MB (14902564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9c2be45293ca0363184f6668c250f7b45c1769a97f44518cbfb30764cc3202`  
		Last Modified: Tue, 31 Aug 2021 03:06:58 GMT  
		Size: 188.7 MB (188731159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a571176bd5f9d2417eec80593ea94b231d38ab0fe2bc86fc37af2feb027d3d`  
		Last Modified: Tue, 31 Aug 2021 05:53:21 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cd240e322d79ebe9c27328edd3744f5fb042f033f1b21800d616a389764832`  
		Last Modified: Tue, 31 Aug 2021 05:53:23 GMT  
		Size: 3.6 MB (3578486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9075a7b52216788a32afc00312ebf29372dd216746b751009ad821540bfed913`  
		Last Modified: Tue, 07 Sep 2021 21:12:11 GMT  
		Size: 44.1 MB (44107112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10625d414603fadf4e8bad30582efb32ccadbbc0ea80efc5bef38d4c86d471a`  
		Last Modified: Tue, 07 Sep 2021 21:11:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk16` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:65f7a57a2d2c97314757418c500cf82b680c9fadf23d340214d81ad794e6491f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295395912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6a7db64887e0bc5d311446e567246ff6e30497b8f79852232cdb459b6609b8`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:02:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:03:48 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 01 Oct 2021 03:03:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:04:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:04:00 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 04:52:03 GMT
CMD ["groovysh"]
# Fri, 01 Oct 2021 04:52:04 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 01 Oct 2021 04:52:04 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Fri, 01 Oct 2021 04:52:04 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 01 Oct 2021 04:52:05 GMT
WORKDIR /home/groovy
# Fri, 01 Oct 2021 04:52:12 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:52:12 GMT
ENV GROOVY_VERSION=3.0.9
# Fri, 01 Oct 2021 04:52:37 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Fri, 01 Oct 2021 04:52:37 GMT
USER groovy
# Fri, 01 Oct 2021 04:52:39 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f9c84d32763760a8a95b798239bf2dd8423aeb8fb56015ddd90196d483d9f`  
		Last Modified: Fri, 01 Oct 2021 03:06:06 GMT  
		Size: 15.9 MB (15895939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b41883131d7cc7c23ae68983b8b2dd37c78b8680b0a3020b02a4404cff47e4`  
		Last Modified: Fri, 01 Oct 2021 03:08:45 GMT  
		Size: 204.1 MB (204094541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e48e45cbd9ae7557314d0cb6b085a2636d3efb9ab85c213b8dd78a30bab3ff`  
		Last Modified: Fri, 01 Oct 2021 04:59:20 GMT  
		Size: 4.4 KB (4395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaddb4341dc47e18202d052e721db85310eb58d946e9fe63f68b2f9eea38cb6`  
		Last Modified: Fri, 01 Oct 2021 04:59:20 GMT  
		Size: 4.1 MB (4121343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab5e1bdd908778b8bd57c15153ce6aac2d835d1f782351ad6641d0a1343f63a`  
		Last Modified: Fri, 01 Oct 2021 04:59:23 GMT  
		Size: 44.1 MB (44107118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057bfa46667d4af5c66f2fe5431a9eb2320258751c194d4250823d330a55dfb8`  
		Last Modified: Fri, 01 Oct 2021 04:59:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk16` - linux; ppc64le

```console
$ docker pull groovy@sha256:99a418c301d800e11eb977c7f2f73970e9550024063308ef97966a9729469028
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286614770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e54ab3171d36e07310f9e30717b69527af9d2c6c3161a6776ffe0fea57593b`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:40 GMT
ADD file:7e5ee5560faaa801aa10a76122190026f8c1da00c809f4fb6ff441751ba0c90f in / 
# Tue, 31 Aug 2021 02:10:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:31:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:33:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:45 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 31 Aug 2021 02:38:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:38:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 02:38:21 GMT
CMD ["jshell"]
# Tue, 31 Aug 2021 07:09:21 GMT
CMD ["groovysh"]
# Tue, 31 Aug 2021 07:09:26 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 31 Aug 2021 07:09:36 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Tue, 31 Aug 2021 07:09:39 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 31 Aug 2021 07:09:44 GMT
WORKDIR /home/groovy
# Tue, 31 Aug 2021 07:10:25 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Tue, 07 Sep 2021 21:21:15 GMT
ENV GROOVY_VERSION=3.0.9
# Tue, 07 Sep 2021 21:21:37 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Tue, 07 Sep 2021 21:21:41 GMT
USER groovy
# Tue, 07 Sep 2021 21:21:59 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:59390c695558464c51dc1fced64934b549770630192a1639ac6a90f59bd63b13`  
		Last Modified: Tue, 31 Aug 2021 02:14:21 GMT  
		Size: 33.3 MB (33291791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6df1a3e21a26bf9e0775ad823e1762b00bf8c2a0650a891b7860b7fe18741a`  
		Last Modified: Tue, 31 Aug 2021 02:54:54 GMT  
		Size: 17.2 MB (17208636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e268da37e94a97fe3d1e52d0ddb36d2d967b4cfbb780b7bcf9a2f4cf63f281`  
		Last Modified: Tue, 31 Aug 2021 02:57:49 GMT  
		Size: 186.9 MB (186934018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09c281c4e6b2577064b102ae6efa0c87d3adbbf51f0b5d5b46768c85a4c6b5a`  
		Last Modified: Tue, 31 Aug 2021 07:22:19 GMT  
		Size: 4.4 KB (4393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a1590a5eb1e1666b21467ae2a5d35f382755e7db9db4b35202a730f8ab31f0`  
		Last Modified: Tue, 31 Aug 2021 07:22:20 GMT  
		Size: 5.1 MB (5068636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c15dc1a2798e39348b57da36cd30f588fac7f1e6c70f84a1c02b10f20f53e4`  
		Last Modified: Tue, 07 Sep 2021 21:30:21 GMT  
		Size: 44.1 MB (44107124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf96936d7471848a29ebd83ce5975acdaa505e3cdd5c0c6424e24a4c397df85`  
		Last Modified: Tue, 07 Sep 2021 21:30:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk16` - linux; s390x

```console
$ docker pull groovy@sha256:6f2fa43c6e0a28c6076f7f8b1a4c5528f268dc6c14a63d0a20dea3a09f4a015b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270868541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5085c5ec8890f9a8acf1702daba477e2b84dd4a9a2c0e09007a0ebcdc9c511a`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 01 Oct 2021 01:42:28 GMT
ADD file:28b3d1959812d7666f9f73b52562cdaaaf84ff25ce6331995e21c66bb31b0cc2 in / 
# Fri, 01 Oct 2021 01:42:30 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:00:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 02:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:01:57 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 01 Oct 2021 02:02:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3447ec27a6dbd4f3a6180a0d4371bb09aa428c16eea9983e515a7400cc9f5c85';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='20fc395d8ea2659e6407cd4ec233dc4399f61b7610f3a16495deb23c1e3b81df';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8d8e35ca5a7e24f16384bf32b110562921c19b4cfe65969980937bf879462bc6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='421cd44661cdbf0c2da79ab3104c81a1fa171b974038e55b1b3d4a042865588f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='7fdda042207efcedd30cd76d6295ed56b9c2e248cb3682c50898a560d4aa1c6f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 02:02:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 02:02:11 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 03:15:05 GMT
CMD ["groovysh"]
# Fri, 01 Oct 2021 03:15:05 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 01 Oct 2021 03:15:05 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Fri, 01 Oct 2021 03:15:05 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 01 Oct 2021 03:15:06 GMT
WORKDIR /home/groovy
# Fri, 01 Oct 2021 03:15:10 GMT
RUN apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         fontconfig         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:15:10 GMT
ENV GROOVY_VERSION=3.0.9
# Fri, 01 Oct 2021 03:15:16 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Fri, 01 Oct 2021 03:15:17 GMT
USER groovy
# Fri, 01 Oct 2021 03:15:18 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:21245da3aae0a4172d9a415c8ba92069601c8a55fc39b783bce7981e97de1b4d`  
		Last Modified: Fri, 01 Oct 2021 01:44:02 GMT  
		Size: 27.1 MB (27122910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b23a8bdcc3c25fc238593c281d2480b42fe86d322be5a1580ea62c30b309a9`  
		Last Modified: Fri, 01 Oct 2021 02:12:12 GMT  
		Size: 15.7 MB (15739781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e180f65401025eac9d618e3cd0fbe55b4ebb587cade99ac7785da88199aa89e7`  
		Last Modified: Fri, 01 Oct 2021 02:13:56 GMT  
		Size: 179.8 MB (179834116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42fa572ae9d31c5d1c06f017ba836cde40795fd9578ed8206ed3a275106e025`  
		Last Modified: Fri, 01 Oct 2021 03:19:51 GMT  
		Size: 4.4 KB (4395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1677c62fd5a0673d2a8be9a13664ccac6a6adf2eb39c8019576c6f0c316b66f`  
		Last Modified: Fri, 01 Oct 2021 03:19:51 GMT  
		Size: 4.1 MB (4060040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687e90b284e79c66baf09e908282d9f2fba2e6130a23287992bf56b07e25b96d`  
		Last Modified: Fri, 01 Oct 2021 03:19:53 GMT  
		Size: 44.1 MB (44107128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec2320147f79c55ae83ba67c5e687184ea3b7e244f3743a0afd8b378a4483f6`  
		Last Modified: Fri, 01 Oct 2021 03:19:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
