## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:ddee215cafc84926531b25799e80e772b2792fb8b28c78e25428925be2ff88fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:d8e09e15a5ff5cb61ec5ca70ee3db59dd4613e84c3470bf387a482a8c37dc145
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100396622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dff20db0f0427ace2bd0941c01a332d4f0a03f371c2ff95c31840ce38015e89`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:36:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 18:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 18:36:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Feb 2023 18:37:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:37:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 01 Feb 2023 18:37:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 01 Feb 2023 18:37:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 01 Feb 2023 23:40:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Feb 2023 23:40:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 23:40:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 01 Feb 2023 23:40:31 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 23:40:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Feb 2023 23:40:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Feb 2023 23:43:24 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 01 Feb 2023 23:43:24 GMT
ENV TOMCAT_MAJOR=8
# Sat, 25 Feb 2023 00:58:43 GMT
ENV TOMCAT_VERSION=8.5.86
# Sat, 25 Feb 2023 00:58:43 GMT
ENV TOMCAT_SHA512=0fc6da94ec8c83dda6e5f0e7502e25eb35a62993f6ce362a395ce269fbd1a01bd4bc96a55debb49adc48c9647bee9743c5bed8cc2aba9d58968f8e3640b80d1b
# Sat, 25 Feb 2023 00:58:44 GMT
COPY dir:ec6f4e17e0bad8969e207ba7201205e601dea1ac945b81dda9d6adb9b6942cd5 in /usr/local/tomcat 
# Sat, 25 Feb 2023 00:58:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Feb 2023 00:58:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 25 Feb 2023 00:58:50 GMT
EXPOSE 8080
# Sat, 25 Feb 2023 00:58:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872bc32ec5617a90e6f01607828b275e221d2a98d3f1a323f870a45fb8259e67`  
		Last Modified: Wed, 01 Feb 2023 18:41:35 GMT  
		Size: 16.3 MB (16335149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113ab51fa2bd87da904badd16c38565a935eea932a88ae7eb4712a08d6bf2849`  
		Last Modified: Wed, 01 Feb 2023 18:41:58 GMT  
		Size: 41.8 MB (41824142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6e1c647e6497acbc0900bf95e953c2ea930ffe8062610af86771c1aeb6a389`  
		Last Modified: Wed, 01 Feb 2023 18:41:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac15e7041f769ea1b427a8eee47db1642b5c67503204203c01e968a4a3113618`  
		Last Modified: Wed, 01 Feb 2023 23:48:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94f0853d80565c53c005778aec4ba5495c80e870c5cd2fc2a0775484435bbef`  
		Last Modified: Sat, 25 Feb 2023 01:16:03 GMT  
		Size: 11.3 MB (11300905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409387fda95d814162a414153b0c2e95883a6fc3cdd3ba25b0ea75197304add0`  
		Last Modified: Sat, 25 Feb 2023 01:16:02 GMT  
		Size: 2.4 MB (2358081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3171a75a13c4316c85650f4f202e5ed0e06de41a0f2cf9a211e3786021ea0f49`  
		Last Modified: Sat, 25 Feb 2023 01:16:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b6b7b900f99823082bfe2288c5abdb2969d03a358f9c9f32625f34c332235e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92529511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35c0fb2881e1eb8ca003c61776b928559a9c3529715b5fec494eeb797aafa91`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:29:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 18:29:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 18:29:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Feb 2023 18:30:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:30:15 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 01 Feb 2023 18:30:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 01 Feb 2023 18:30:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 25 Feb 2023 06:08:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 25 Feb 2023 06:08:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Feb 2023 06:08:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 25 Feb 2023 06:08:18 GMT
WORKDIR /usr/local/tomcat
# Sat, 25 Feb 2023 06:08:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 25 Feb 2023 06:08:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 25 Feb 2023 06:13:38 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 25 Feb 2023 06:13:39 GMT
ENV TOMCAT_MAJOR=8
# Sat, 25 Feb 2023 06:13:39 GMT
ENV TOMCAT_VERSION=8.5.86
# Sat, 25 Feb 2023 06:13:39 GMT
ENV TOMCAT_SHA512=0fc6da94ec8c83dda6e5f0e7502e25eb35a62993f6ce362a395ce269fbd1a01bd4bc96a55debb49adc48c9647bee9743c5bed8cc2aba9d58968f8e3640b80d1b
# Sat, 25 Feb 2023 06:13:39 GMT
COPY dir:11ae6cb6d8168812e9e8f60667238b49f921125307f1c3c20e0399b432c45b68 in /usr/local/tomcat 
# Sat, 25 Feb 2023 06:13:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Feb 2023 06:13:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 25 Feb 2023 06:13:44 GMT
EXPOSE 8080
# Sat, 25 Feb 2023 06:13:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:316383d79e03258e1fee780854f6da78da364194ded4ace8bff50687070e1c8f`  
		Last Modified: Sat, 28 Jan 2023 04:40:09 GMT  
		Size: 24.6 MB (24586318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c95448bcd85b50b98d91a76e25906548e7ff17609a31915862d7033738c1a3`  
		Last Modified: Wed, 01 Feb 2023 18:36:26 GMT  
		Size: 15.2 MB (15174549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a670aeba2a1e2c271bb11404f02b3d10678970e6a052a361a7e538d935b2115`  
		Last Modified: Wed, 01 Feb 2023 18:36:53 GMT  
		Size: 39.5 MB (39545154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6179766e30e542ce487e687fcb8908fd48b0bf63207f46cec995f05e55c29f`  
		Last Modified: Wed, 01 Feb 2023 18:36:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fd557a260241ab33c91d26b667e43a0415ea5bee7bc13373b13ab30ea2128a`  
		Last Modified: Sat, 25 Feb 2023 06:31:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1644cd4239dcfd49d99adb55845ff5d32cc68586e8b918199a5e357b440d5858`  
		Last Modified: Sat, 25 Feb 2023 06:36:01 GMT  
		Size: 11.2 MB (11249511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8725ccba1c2c7f84db834181d04d245f60d9f62d0be874611b86bf6b8b8d4a21`  
		Last Modified: Sat, 25 Feb 2023 06:36:00 GMT  
		Size: 2.0 MB (1973548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac2b1802028cafce2c74e2e78c2ae7f7ce6f324fb88c1c97a63b57ee0268337`  
		Last Modified: Sat, 25 Feb 2023 06:36:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:efe8d3ca10d7bcd9f296366986d872f5c57f1d30b6d265376515a1117a72172e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95979146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8fd6d242420142b1331e6412036c87bad8295291fa7f60dd2089579c55781`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:27:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:27:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:27:29 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:28:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 07:48:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 Mar 2023 07:48:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:48:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 Mar 2023 07:48:38 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 Mar 2023 07:48:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 Mar 2023 07:48:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 Mar 2023 07:52:59 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 02 Mar 2023 07:52:59 GMT
ENV TOMCAT_MAJOR=8
# Thu, 02 Mar 2023 07:52:59 GMT
ENV TOMCAT_VERSION=8.5.86
# Thu, 02 Mar 2023 07:53:00 GMT
ENV TOMCAT_SHA512=0fc6da94ec8c83dda6e5f0e7502e25eb35a62993f6ce362a395ce269fbd1a01bd4bc96a55debb49adc48c9647bee9743c5bed8cc2aba9d58968f8e3640b80d1b
# Thu, 02 Mar 2023 07:53:00 GMT
COPY dir:6c7c8c689f8a0264e3fcb2b3a372750eb2b7b9345a21e3f4910f0060dbf49160 in /usr/local/tomcat 
# Thu, 02 Mar 2023 07:53:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:53:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 Mar 2023 07:53:04 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 07:53:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56953e7d42aaef3e68834ce3dfeea50f3d10b770bf02cf88d1e4948eb585e4a2`  
		Last Modified: Thu, 02 Mar 2023 04:33:09 GMT  
		Size: 16.2 MB (16210001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419759787943a785f583388240379f8fdb99d0447a875ba1f6755577ee6c60b9`  
		Last Modified: Thu, 02 Mar 2023 04:33:44 GMT  
		Size: 40.8 MB (40808822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011f8d1b818a37dabe28784bf456f56b1cdb4cc330d1aba02eaf1df506add6d`  
		Last Modified: Thu, 02 Mar 2023 04:33:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a5bc9d145051f89966de36cead594d0b724d41863f2c36d8b43d90e4c14ed8`  
		Last Modified: Thu, 02 Mar 2023 08:03:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b0961f844f00cb2ac7e7140d18499dba5236ee52f781a7ae1746ad09eae4a0`  
		Last Modified: Thu, 02 Mar 2023 08:07:23 GMT  
		Size: 11.3 MB (11317426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e944b3cc412c6bc126c930b87fec945fbdfb7fba24c3af4bb70a4ba5ee6482`  
		Last Modified: Thu, 02 Mar 2023 08:07:23 GMT  
		Size: 447.9 KB (447911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93400a8601f9139a6c987250621c9bc67352399ffb9e83cc38e05db8ee165b45`  
		Last Modified: Thu, 02 Mar 2023 08:07:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f1a8b63e05207c455c37aa8d9b663674889dafe3828ab14b1fab71daa0adbebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103909156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3164016944c8e8975da41ffb5e36845fb83f1842c88196c92b95bde93c9c6c3d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:04:16 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 02 Mar 2023 04:06:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cbe45788fa2d9d04d6b10f8aec7dbb15a018dbafe897ed75e31876d0367d56a5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='82d8524838b07ee438d42f4c33b6ecfe89ae83efac9af0605c76d75195bdcd99';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5ec3e07126fedc23b58bb0f5b2dd05b5e9599ce1a3567fc2c7b27587f39faa3b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c8c4e180f915fc7c163240bf363dcdf2b481cd2723fabfc3d08ccf12e049611f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jre_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Mar 2023 04:06:20 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 02 Mar 2023 06:55:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 Mar 2023 06:55:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 06:55:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 Mar 2023 06:55:08 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 Mar 2023 06:55:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 Mar 2023 06:55:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 Mar 2023 07:12:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 02 Mar 2023 07:12:08 GMT
ENV TOMCAT_MAJOR=8
# Thu, 02 Mar 2023 07:12:09 GMT
ENV TOMCAT_VERSION=8.5.86
# Thu, 02 Mar 2023 07:12:09 GMT
ENV TOMCAT_SHA512=0fc6da94ec8c83dda6e5f0e7502e25eb35a62993f6ce362a395ce269fbd1a01bd4bc96a55debb49adc48c9647bee9743c5bed8cc2aba9d58968f8e3640b80d1b
# Thu, 02 Mar 2023 07:12:10 GMT
COPY dir:eb8d39162872e4e9caf07759927cb561f861355589cb4b3401803cfa923eeb58 in /usr/local/tomcat 
# Thu, 02 Mar 2023 07:12:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:12:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 Mar 2023 07:12:24 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 07:12:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ed241fb085c44d6c1e8d524e97350ed5286126d2020db5d72908a99d4af45a`  
		Last Modified: Thu, 02 Mar 2023 04:18:38 GMT  
		Size: 41.2 MB (41214796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ee1da147a00b751df8204f38135873b823769f0338ecf653213ebc1a25c7cf`  
		Last Modified: Thu, 02 Mar 2023 04:18:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf9200e82594a3f509ba24e961012bdfb56ee05e03ad4201248d94c4b797d3d`  
		Last Modified: Thu, 02 Mar 2023 07:28:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7c27406af2538c3350762815703374d154e38ce57483b5b2e83f78b01f336`  
		Last Modified: Thu, 02 Mar 2023 07:33:24 GMT  
		Size: 11.3 MB (11341729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d95c18e19e45aa5a52335886b2f8618c6bb76fa467c19e6df12f5ff6857a9e`  
		Last Modified: Thu, 02 Mar 2023 07:33:22 GMT  
		Size: 473.9 KB (473948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0681d8a0e01c7706657727a01a03968bcf5bd8361db1daea522e5acc5302bc`  
		Last Modified: Thu, 02 Mar 2023 07:33:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
