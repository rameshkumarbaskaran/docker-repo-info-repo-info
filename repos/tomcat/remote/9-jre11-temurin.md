## `tomcat:9-jre11-temurin`

```console
$ docker pull tomcat@sha256:da6399d91bf3fb2dedc5a99c4102897b25d7d6a25c4de993b1555dd26c4c5b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:c3117850e025a347eb18b5bf259f2dcb805be1f8c19cabff810d7e322b407880
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102948338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4be2a065283abc1f57162aeb001c4a8449f3c30d520c044d3d2b44363acff9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:37:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:37:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:37:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:37:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:38:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Sat, 02 Sep 2023 00:39:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:39:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:39:05 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:39:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 03:43:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 03:43:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 03:43:15 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 03:43:15 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 03:43:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:43:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:44:59 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Sep 2023 03:44:59 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Sep 2023 03:44:59 GMT
ENV TOMCAT_VERSION=9.0.80
# Sat, 02 Sep 2023 03:44:59 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Sat, 02 Sep 2023 03:44:59 GMT
COPY dir:d7e211ba43c9ae41c4526bf9dad571066be23b7faa3126c3d0bf989be5e2e4ea in /usr/local/tomcat 
# Sat, 02 Sep 2023 03:45:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 03:45:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 03:45:05 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 03:45:05 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 03:45:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274fb0278626020650ff7c358074255903c792176a61a1ebce3055ba27e11436`  
		Last Modified: Sat, 02 Sep 2023 00:41:34 GMT  
		Size: 12.9 MB (12902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00346ef46b0fe8a50b11fd9621a92a596760afe94bc7f1941e884d97e4b239a1`  
		Last Modified: Sat, 02 Sep 2023 00:42:41 GMT  
		Size: 46.9 MB (46864483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e407e98debb8151066db1e98639d0fc3cfe04dab507e3d032537a64ecd85d4`  
		Last Modified: Sat, 02 Sep 2023 00:42:34 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4075bbc4ec0f48ded2ad33e229d3a85fd6c61f3acf35c85fd6a6ce8fd1dd44b7`  
		Last Modified: Sat, 02 Sep 2023 00:42:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0760623340fc44750aa3df57005e382ac8671c2492e6f7f6f89ee0ab6b5b4cd`  
		Last Modified: Sat, 02 Sep 2023 03:52:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303afc506abfa7a02c475d50c1fe0b3dbfd7a5335bd16d58e8bd16022579a26`  
		Last Modified: Sat, 02 Sep 2023 03:54:17 GMT  
		Size: 12.3 MB (12285235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed7f0b9c144157fea85e22faf7262fc3aec6b708240de7524e48e8d0efb7c48`  
		Last Modified: Sat, 02 Sep 2023 03:54:16 GMT  
		Size: 455.6 KB (455564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571d84ab4f37d729996290f14196965ed60f9d24192faf3f4a011fb5b0d0edc9`  
		Last Modified: Sat, 02 Sep 2023 03:54:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:a7526b7ad4b9a5ab8703124d1d5f4e7394ca16e3457fd5e8ad3bff90268ca34e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97667290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd7f98bcd353021dbfe9bd9211bd63675f2840ef8e785cecbed1a644faae821`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 25 Sep 2023 10:19:15 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:19:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:19:18 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Mon, 25 Sep 2023 10:19:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:00:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:00:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:01:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Tue, 03 Oct 2023 06:02:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:02:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:02:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:02:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:56:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 06:56:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:56:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 06:56:16 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 06:56:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:56:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:57:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Oct 2023 06:57:45 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Oct 2023 06:57:45 GMT
ENV TOMCAT_VERSION=9.0.80
# Tue, 03 Oct 2023 06:57:45 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Tue, 03 Oct 2023 06:57:46 GMT
COPY dir:a03703c01e820970938fb3dbf5257e0ae1e60dc2ec44a03dd930242ee28787b6 in /usr/local/tomcat 
# Tue, 03 Oct 2023 06:57:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:57:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 06:57:52 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 06:57:52 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 06:57:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7271b2c80df6c73d794550b50f57d78c6fd5b85da7934c6506c76ea706087280`  
		Last Modified: Tue, 26 Sep 2023 02:07:56 GMT  
		Size: 27.5 MB (27515498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda8dd86380daebf30969cb41ed0b268657958a7e1447d39fc3a2fc0d9c8c636`  
		Last Modified: Tue, 03 Oct 2023 06:03:57 GMT  
		Size: 12.5 MB (12491478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72f496e54e741199b5cf52fb27d70d5e8b72cab406852a0a971af0fda8b7077`  
		Last Modified: Tue, 03 Oct 2023 06:05:03 GMT  
		Size: 45.0 MB (45012599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7f8cf124bd8e3b73376ff7a7f099bb0296ee827fb2a0effa3d680e6cf6bd42`  
		Last Modified: Tue, 03 Oct 2023 06:04:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404aca9dcfb64a64d8574f380cb6e9c20dc67bc15bdf62b297eb673f3ee695`  
		Last Modified: Tue, 03 Oct 2023 06:04:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d25e01a80defe6e28f3d9c94e275f74b26f542917d577f08adc9d21b38fb4ca`  
		Last Modified: Tue, 03 Oct 2023 07:04:52 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b294a70c8dfa3c3b1303545108efcdd8f5a8d6536a31da3795a3a4bfa5c432cf`  
		Last Modified: Tue, 03 Oct 2023 07:06:51 GMT  
		Size: 12.2 MB (12216701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ce2c1efbb46417ccbdce3ae62e190efc1a29ad519a50bd228d61080c80221e`  
		Last Modified: Tue, 03 Oct 2023 07:06:50 GMT  
		Size: 429.8 KB (429818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588d8d0bf1bd5598b1b61a0bf88c81de88e6e02258c5c0a61cefd37fb2f15a62`  
		Last Modified: Tue, 03 Oct 2023 07:06:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b90ff68938538063ceb15d3e322112a77c7ed6ca07e1c3f7b34963074b32276d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99175133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb461a31d0d9c0d947a7cc1df2c0d3b4bd45eef930226d0f4a5438dbbb02da66`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:06:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:07:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:07:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Tue, 03 Oct 2023 06:07:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:07:59 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:07:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:07:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 07:49:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 07:49:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 07:49:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 07:49:54 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 07:49:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:49:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:51:23 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Oct 2023 07:51:23 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Oct 2023 07:51:23 GMT
ENV TOMCAT_VERSION=9.0.80
# Tue, 03 Oct 2023 07:51:23 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Tue, 03 Oct 2023 07:51:23 GMT
COPY dir:f3d8db3f72bd4112aa6df17ef9fb739333232b733996749ca9b4f812e3761eba in /usr/local/tomcat 
# Tue, 03 Oct 2023 07:51:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:51:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 07:51:28 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 07:51:28 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 07:51:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904450c39fc4ef39317a37a19b15df4a74bf6bb91100343e382470ce034d79`  
		Last Modified: Tue, 03 Oct 2023 06:10:10 GMT  
		Size: 12.8 MB (12843603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30912c039dbaa796a9a5ed542699bef3d9a28d45ef6fffa82c09a17c4052a8fb`  
		Last Modified: Tue, 03 Oct 2023 06:11:17 GMT  
		Size: 45.2 MB (45190639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4baa5de8169875cf5865d296a609c50890a7399b643ee1c70d96c34858f22`  
		Last Modified: Tue, 03 Oct 2023 06:11:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ccb257c1839235e5d23765c7e3a1a38f9d8f26fcb582bf489b3092f6ba4f59`  
		Last Modified: Tue, 03 Oct 2023 06:11:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe014e40db5b2327ab56545990d7cccba870416075c416bbb42e125a013345c`  
		Last Modified: Tue, 03 Oct 2023 07:59:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b410552bb31848e6f47e2d8e27147e5fd10d3ee98e6a0340b8ea40a8c57324`  
		Last Modified: Tue, 03 Oct 2023 08:01:11 GMT  
		Size: 12.3 MB (12291673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e050b1d52e78eb9b1fc0f9d8cf7f3f2538ff93b3dca6d15c442f8d9583ce991`  
		Last Modified: Tue, 03 Oct 2023 08:01:11 GMT  
		Size: 455.9 KB (455950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f6ba6f799226d3661cde93867cae36e45341b5074c20dfd54e6c2915eaa86a`  
		Last Modified: Tue, 03 Oct 2023 08:01:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:18163ff549c32c88a4d8ef176fe80b0672e8d42f8d5bb8cdad983d4a16edbe62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104571692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee936882328a524a5dff5cbf25139c09573f08d40f4321a1797d0b610edb21b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:03:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:03:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:04:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:05:08 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Sat, 02 Sep 2023 00:05:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:05:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:05:56 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:05:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 02:19:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 02:19:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 02:19:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 02:19:41 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 02:19:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:19:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:25:01 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Sep 2023 02:25:02 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Sep 2023 02:25:02 GMT
ENV TOMCAT_VERSION=9.0.80
# Sat, 02 Sep 2023 02:25:02 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Sat, 02 Sep 2023 02:25:03 GMT
COPY dir:71006b09ed71ac0e4509db58036b381d3d75e2482cd988aab6dd045036df9e2c in /usr/local/tomcat 
# Sat, 02 Sep 2023 02:25:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 02:25:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 02:25:18 GMT
EXPOSE 8080
# Wed, 13 Sep 2023 00:47:18 GMT
ENTRYPOINT []
# Wed, 13 Sep 2023 00:47:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bbdfadf6550699bed2516a6d795d42d07af539ddc96ec121092535bbfefc27`  
		Last Modified: Sat, 02 Sep 2023 00:08:53 GMT  
		Size: 13.8 MB (13770760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dd1f607f3771d23b6b7cad047abbf6c75f5669bc17404780753ee03ee828bd`  
		Last Modified: Sat, 02 Sep 2023 00:10:34 GMT  
		Size: 42.3 MB (42294912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8760e0a0a07cdc9292a64be5d7008c7f26b688ca2dc5c4d1127d692ae1740216`  
		Last Modified: Sat, 02 Sep 2023 00:10:24 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ce78ab1d55161c10a01105f9b7bfd5415eae3237ff91bf57c47cc330171ed`  
		Last Modified: Sat, 02 Sep 2023 00:10:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae1024ecaa03521ace5221415e31565292b5f8f2396db80814030db79edef71`  
		Last Modified: Sat, 02 Sep 2023 02:40:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaa1c24b485f5c269ba2693c3a7b2a1e8d714d4d800598ac0c84d3be4ef5a85`  
		Last Modified: Sat, 02 Sep 2023 02:43:24 GMT  
		Size: 12.3 MB (12312180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97efcbe8f377d187af0fbf841398d3cf6e0bca5c47e5f3e9b79b68c95c67eb9`  
		Last Modified: Sat, 02 Sep 2023 02:43:23 GMT  
		Size: 487.0 KB (486990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd25ea951f4e456d9eaa0764d9509836286fa44d7ec0a002de404a6a9324623`  
		Last Modified: Sat, 02 Sep 2023 02:43:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:f3dcccbdfd0199a203045d69fc2d1d1591b0cfd4467d5f5444f1651e01d0dbe8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94995672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f72970922269d7db5001cf66bcb7a5aa9dc9b595bc81358f56d76944bdc832a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:26:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:26:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:26:25 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Fri, 01 Sep 2023 23:27:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:27:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:27:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:27:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 00:29:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 00:29:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:29:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 00:29:37 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 00:29:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:29:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:31:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Sep 2023 00:31:40 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Sep 2023 00:31:40 GMT
ENV TOMCAT_VERSION=9.0.80
# Sat, 02 Sep 2023 00:31:40 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Sat, 02 Sep 2023 00:31:41 GMT
COPY dir:545d0888213253ee7d33898d6700be93f1e4a623b7f6ee4709ceb2e66884fb94 in /usr/local/tomcat 
# Sat, 02 Sep 2023 00:31:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:31:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 00:31:47 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 00:31:47 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 00:31:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed43a5cfb5c9e6c7002428dd4158a94eb479db0389f441f36b1fbf8dd485745e`  
		Last Modified: Fri, 01 Sep 2023 23:29:08 GMT  
		Size: 13.0 MB (12981971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb7971e2d778fe704c19699f891f62891f2bdad2041ef29918e015d6be79383`  
		Last Modified: Fri, 01 Sep 2023 23:29:29 GMT  
		Size: 40.6 MB (40631464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5922fcb2555642cdecd4bed8006dc80ab251ad0c5b44d9f2480aea61bcbcdd31`  
		Last Modified: Fri, 01 Sep 2023 23:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d643aeaf255f58ad1ed3432d32433d501d5548caa07c02601b0694416d2024`  
		Last Modified: Fri, 01 Sep 2023 23:29:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594b0f42040dc559aa89103c134e11cb160667b4a6ff14f9779ffad71d4dff30`  
		Last Modified: Sat, 02 Sep 2023 00:36:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9caff4ec279f70b0d4c995128fefb84682e6878d2fac8a13e98f0fe2506d902`  
		Last Modified: Sat, 02 Sep 2023 00:37:41 GMT  
		Size: 12.3 MB (12278036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35c1879e8cda48afc7e9db30267e560e4aaff4796771e54a707c064c39f156b`  
		Last Modified: Sat, 02 Sep 2023 00:37:36 GMT  
		Size: 457.2 KB (457171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe021affafe1ce7fdbc0be870de20b006013eb04f62fc31fe55b1a268df5411`  
		Last Modified: Sat, 02 Sep 2023 00:37:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
