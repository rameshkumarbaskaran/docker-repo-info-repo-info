## `maven:3-eclipse-temurin-19`

```console
$ docker pull maven@sha256:7ead36f5ab9c0d8c34b7be20119d0ff2ca6139e611834a083e8f5228bbb6f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-19` - linux; amd64

```console
$ docker pull maven@sha256:4632d6116ff6019728148c865bdeade233ad4039e9bac621b2145b482fc6da01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278685946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68755848798e6c70fc9b86c61f4a829e00b7468d440711a8c385fb60b0cefef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:45:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:22:38 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Wed, 25 Jan 2023 19:22:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 25 Jan 2023 19:22:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 25 Jan 2023 19:22:50 GMT
CMD ["jshell"]
# Wed, 25 Jan 2023 20:25:04 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:25:05 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 25 Jan 2023 20:25:05 GMT
ARG USER_HOME_DIR=/root
# Wed, 25 Jan 2023 20:25:05 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 25 Jan 2023 20:25:05 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 25 Jan 2023 20:25:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 25 Jan 2023 20:25:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 25 Jan 2023 20:25:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 25 Jan 2023 20:25:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 25 Jan 2023 20:25:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 25 Jan 2023 20:25:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 25 Jan 2023 20:25:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8d923227d8dc300e1ddab1b65c83c0eff7f4a7105d958420872f7138b79735`  
		Last Modified: Fri, 09 Dec 2022 01:52:47 GMT  
		Size: 17.0 MB (16973851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50237d5a66d7b378095155ca8b2422b9ab7832032b9f89fc71095ec98c9b3a0`  
		Last Modified: Wed, 25 Jan 2023 19:29:52 GMT  
		Size: 201.1 MB (201116681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556d3d2d13a6d28959c08864b80cd2dd946512ca28fb01a2516b051eb251491e`  
		Last Modified: Wed, 25 Jan 2023 19:29:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a301ff3ca27bce29171bd9deb385e98aa4b8da665f8080fb7011f51252fd6b7`  
		Last Modified: Wed, 25 Jan 2023 20:28:05 GMT  
		Size: 21.8 MB (21814168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a856029e4ccbd5985ed8cb3f618b8580acc245aa51a575ff2b0b33da3081e43`  
		Last Modified: Wed, 25 Jan 2023 20:28:02 GMT  
		Size: 8.4 MB (8351151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50067a2eaa74c92e6a75b9636f4d165e34c330e92540cefd1fcfdce8663623cc`  
		Last Modified: Wed, 25 Jan 2023 20:28:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b88ead1e6d71ca5e1a0c7ff192a28995f99671dc753b15d06dda0c8f78b993`  
		Last Modified: Wed, 25 Jan 2023 20:28:01 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-19` - linux; arm variant v7

```console
$ docker pull maven@sha256:719b7be1bad07cc737fdd56ccf69babb577b2d5d265921994fe8f0bd21e77680
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275402075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0027969a634518dbd2b7f9d6e67c45f72f761a4b2fa80493ff41a90c6d81e7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:54:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 18:54:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:54:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:59:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:00:48 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Tue, 31 Jan 2023 19:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 19:01:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 19:01:03 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 21:26:25 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:26:25 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 21:26:25 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 21:26:26 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 21:26:26 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 21:26:28 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 21:26:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 21:26:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 21:26:28 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 21:26:28 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 21:26:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 21:26:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d0210273e3495988f639f6164118a5bba55666799ba86ac3e60a001cf7be3b31`  
		Last Modified: Thu, 26 Jan 2023 18:27:33 GMT  
		Size: 27.0 MB (27022323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7067739b4b4dafc215ce018bfdf1796e600c263337e1e8344fa69590d873c202`  
		Last Modified: Tue, 31 Jan 2023 19:07:34 GMT  
		Size: 17.1 MB (17092113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9c423fb5b1d836c11b072aabd848106c58e31000053f6ef62aba6319ac7b5a`  
		Last Modified: Tue, 31 Jan 2023 19:09:39 GMT  
		Size: 197.6 MB (197564217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a7fa6703e67420eb6cf5231e83f8b3b13915a1ae2f15357928054fb747bc5e`  
		Last Modified: Tue, 31 Jan 2023 19:09:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d036d931dd9c0abc9750613ba2cb82e317eac6b8216eb93c1f1136eecf795`  
		Last Modified: Tue, 31 Jan 2023 21:30:37 GMT  
		Size: 25.4 MB (25370899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78da500644646c93319bd37af2b1b514aab471433b265280c31ce10fecfdc748`  
		Last Modified: Tue, 31 Jan 2023 21:30:33 GMT  
		Size: 8.4 MB (8351137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50715051c788ca3dcfb754ed827782c3932055740b72ecc25ece48e98c224114`  
		Last Modified: Tue, 31 Jan 2023 21:30:32 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b234fece1a4862025d8e29ac694db78a100e887199351f775b3f6c82df267c`  
		Last Modified: Tue, 31 Jan 2023 21:30:32 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-19` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:778df1b449beb81a9ab1c4cabfddb6134c155915d96e895e3ef7601308292bd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276750015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f1ca7d428152afe849ca0c0d247672f62b4622a783af834c72c63cc76a3f5a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:57 GMT
ADD file:429a55a11d4bcd15647d1316d9debd9ead4b4ab5c0b9146894d07c39aa814290 in / 
# Fri, 09 Dec 2022 01:46:57 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:39:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:39:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:39:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:42:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 18:41:32 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Wed, 25 Jan 2023 18:41:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 25 Jan 2023 18:41:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 25 Jan 2023 18:41:43 GMT
CMD ["jshell"]
# Wed, 25 Jan 2023 20:23:34 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:23:34 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 25 Jan 2023 20:23:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 25 Jan 2023 20:23:34 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 25 Jan 2023 20:23:34 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 25 Jan 2023 20:23:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 25 Jan 2023 20:23:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 25 Jan 2023 20:23:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 25 Jan 2023 20:23:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 25 Jan 2023 20:23:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 25 Jan 2023 20:23:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 25 Jan 2023 20:23:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f2e5e37e706412c1481b71d2240df4fe659ef83ae4d2932a8ddfe42b0d3d20`  
		Last Modified: Fri, 09 Dec 2022 03:48:04 GMT  
		Size: 18.4 MB (18400373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bb33cc73bba5543810a02f2a8cc04e8eb4950651cd9dd4c2465979ed17558`  
		Last Modified: Wed, 25 Jan 2023 18:47:15 GMT  
		Size: 199.9 MB (199867843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9a9acf7d6cc9cf094d9005ed8e403fe05051c45962817c831029295fc4fff0`  
		Last Modified: Wed, 25 Jan 2023 18:47:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960bab9db6d17727627acbffc1723e740610fba900b618cdd432e3d0ec9db8fc`  
		Last Modified: Wed, 25 Jan 2023 20:25:40 GMT  
		Size: 21.7 MB (21744765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00192b07531dfe0e6d1bb1d2e2813198b41501097425024787b3cacb58adb6`  
		Last Modified: Wed, 25 Jan 2023 20:25:38 GMT  
		Size: 8.4 MB (8351174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46fbdc6a996904a3baa17788b8e2c663afee7d29dc6d7f5399c2291b311a4f4`  
		Last Modified: Wed, 25 Jan 2023 20:25:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71472beb7d3adb3e94005ad98037afc6fe54a93951496a8414a33fad74d008e`  
		Last Modified: Wed, 25 Jan 2023 20:25:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-19` - linux; ppc64le

```console
$ docker pull maven@sha256:4c10dcd45d314b127b4fe59d3142a085ea290978e94e1e2397daa374a7fbcca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288285784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ee627bb723d041f9ade19378fdb18ef905cd0a8fffb87de36d28434c38340f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:45:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:51:15 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Wed, 25 Jan 2023 19:51:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 25 Jan 2023 19:51:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 25 Jan 2023 19:51:42 GMT
CMD ["jshell"]
# Wed, 25 Jan 2023 20:41:33 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:41:34 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 25 Jan 2023 20:41:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 25 Jan 2023 20:41:35 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 25 Jan 2023 20:41:35 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 25 Jan 2023 20:41:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 25 Jan 2023 20:41:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 25 Jan 2023 20:41:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 25 Jan 2023 20:41:38 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 25 Jan 2023 20:41:38 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 25 Jan 2023 20:41:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 25 Jan 2023 20:41:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b742749281388888fe53f807ad7ae6b5c091713777c43c8f4f21cc50f873d5`  
		Last Modified: Fri, 09 Dec 2022 02:57:27 GMT  
		Size: 18.3 MB (18256829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc43d9265fcc00f35fe810ec1c6107c8884ebf1643cdeef18b744737a54d980`  
		Last Modified: Wed, 25 Jan 2023 20:02:00 GMT  
		Size: 200.3 MB (200290300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33d18db22a0b79ce29546d103e52fe2259f984068babd4544f14ac05e7abac8`  
		Last Modified: Wed, 25 Jan 2023 20:01:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb3338c2660950e53cb85d45d2720bf970463ba134cc5ce1a5faec7d77c8bf6`  
		Last Modified: Wed, 25 Jan 2023 20:45:10 GMT  
		Size: 25.7 MB (25677965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a0576a76d7165de4529088192344d6860c3f7fade6c8f5ca8379a9c0f9821f`  
		Last Modified: Wed, 25 Jan 2023 20:45:04 GMT  
		Size: 8.4 MB (8351147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933e0d9c4e33dc7fe28187a40a442e174d2e51629d8a6a41e7f99ea1a86eba16`  
		Last Modified: Wed, 25 Jan 2023 20:45:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080d02d354dd0ccf6ef6e1e64e64a20648a4872613e717fbb89f86b1bb538735`  
		Last Modified: Wed, 25 Jan 2023 20:45:03 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-19` - linux; s390x

```console
$ docker pull maven@sha256:384f6c3fb56d95976bee89aec151c1e3c4f72eaa6d4f4aab3b15a95082fc90bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264208836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4500e54f6cd95648b746c125d4b24db67ff19ea441f024ead40fabb8cd95e3c3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:59:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:59:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:59:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:00:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:02:18 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Tue, 31 Jan 2023 18:02:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        armhf|arm)          ESUM='6a51cb3868b5a3b81848a0d276267230ff3f8639f20ba9ae9ef1d386440bf1fd';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_arm_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 31 Jan 2023 18:02:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 31 Jan 2023 18:02:33 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 19:47:10 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:47:12 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 19:47:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 19:47:12 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 19:47:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 19:47:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 19:47:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 19:47:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 19:47:22 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 19:47:22 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 19:47:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 19:47:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dd969ed9de43018fe5442c859bf66eabf23145b966b9338392ea707aed18b26f`  
		Last Modified: Tue, 31 Jan 2023 17:55:34 GMT  
		Size: 28.6 MB (28641926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028897ef38647e3545f5404bcb21a993ff6d9f6d87aeabe064f00b3df6f0d4cf`  
		Last Modified: Tue, 31 Jan 2023 18:06:38 GMT  
		Size: 16.8 MB (16753131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb32dfb86fb4b0504e43d43e47a033313123ee1c1079c19e3eb04bd44cb9eaf2`  
		Last Modified: Tue, 31 Jan 2023 18:08:02 GMT  
		Size: 188.5 MB (188510631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d2cd3e791fb56569e345ee6bdad1123439a68e094c55339d23ec4ff79d1cc2`  
		Last Modified: Tue, 31 Jan 2023 18:07:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709933fa07a214d6ec0b48fed39a03f34250afd59d9d1bb30eddecb52d07f674`  
		Last Modified: Tue, 31 Jan 2023 19:51:34 GMT  
		Size: 22.0 MB (21950624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44256b6104ed99f5b0b75f82d31bb439e175751dc7a20b0b79550a3bcc69d3f6`  
		Last Modified: Tue, 31 Jan 2023 19:51:31 GMT  
		Size: 8.4 MB (8351138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0792773df3146ba4680d8cb8724a8868c77191fa9a5e0813eb566dc2167588`  
		Last Modified: Tue, 31 Jan 2023 19:51:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a7f7ae802265ec3b0c092e89b8670f1f0065a32d93f3b167009518bc38c8f8`  
		Last Modified: Tue, 31 Jan 2023 19:51:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
