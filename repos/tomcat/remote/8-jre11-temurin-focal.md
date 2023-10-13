## `tomcat:8-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:12d9ba13efd90e49bb4a261191fa0078e3e2cfe5b2cd789e5958c0ba26671b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:8-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:9e2536abffebf9f692288234ddbdaba58da1d9c5358975d3407add39c6f3641e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104242240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e8da0675ee23e211326d62d5e529b1f6b76c69442cf4a9f7067db09842d97`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:20:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:21:53 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:23:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:23:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:23:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:23:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 22:33:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 22:33:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:33:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 22:33:41 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 22:33:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:33:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:37:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 31 Aug 2023 22:37:29 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 00:35:12 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 00:35:13 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 00:35:13 GMT
COPY dir:cc6bf0108d23ca6a5d47a2d3426f9fec8602b3835a339c31466c704ce7637db7 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:35:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:35:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:35:19 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:35:19 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:35:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32e041863d53bbb7f9f65ba31f023a9f344dd4105bf5345c6e748e3cc3e71a`  
		Last Modified: Tue, 08 Aug 2023 19:26:48 GMT  
		Size: 16.9 MB (16919807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c387219ad28fcaaa0c3f8710f193db936ab43a235d039af3db34c2a14040036`  
		Last Modified: Thu, 31 Aug 2023 20:29:01 GMT  
		Size: 46.9 MB (46862612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b06dad35039dc686d67206c6b2aa63a5b44238cce2a245d21b2a08e1f81344`  
		Last Modified: Thu, 31 Aug 2023 20:28:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1818ec198c0ec424a918ba07db49f776ace1c7ee14e13cfc6e4c437f6fa8819`  
		Last Modified: Thu, 31 Aug 2023 20:28:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cac76c9436430f6ec2bea6ab0ac953626c8bb5bb50b97226424ca6a9ee8ddf`  
		Last Modified: Thu, 31 Aug 2023 22:44:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282de109ef2b04dcc5fec97c7e9fc8ae1953846c76d749114ab2578a58b8bd38`  
		Last Modified: Fri, 13 Oct 2023 00:57:09 GMT  
		Size: 11.4 MB (11428376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e9bf3facba84c585038eca4e9c37b95510dfa1464ca5944884b908246b003e`  
		Last Modified: Fri, 13 Oct 2023 00:57:08 GMT  
		Size: 449.6 KB (449580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40247331dc3801ce9909111e13e2e7ddb6cc0987a3a5945697cdc5f2f30a18bd`  
		Last Modified: Fri, 13 Oct 2023 00:57:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:d64b6d57d3b0b1e9823f8c3c905b39d60a9db9970e09e7fd8000ed8634451cd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97068036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3054aba5fd518d46485dd6b5db4e2e959e2c70344d0a4fe0cf480b2168bd1065`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:15:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 01:15:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:16:59 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Fri, 13 Oct 2023 01:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 01:17:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 01:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 01:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Oct 2023 04:25:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 13 Oct 2023 04:25:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 04:25:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 13 Oct 2023 04:25:42 GMT
WORKDIR /usr/local/tomcat
# Fri, 13 Oct 2023 04:25:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 13 Oct 2023 04:25:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 13 Oct 2023 04:30:36 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 13 Oct 2023 04:30:36 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 04:30:36 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 04:30:36 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 04:30:37 GMT
COPY dir:037a1c0670b872b46cbdf928e7abb4b9e686199984577246848b92e4a1a08058 in /usr/local/tomcat 
# Fri, 13 Oct 2023 04:30:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:30:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 04:30:42 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 04:30:42 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 04:30:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2807e7ba722152aeebf6e73ef8d6ba6473d71ef34b3c32b67bc40d66aa1f4e07`  
		Last Modified: Fri, 13 Oct 2023 01:20:27 GMT  
		Size: 15.7 MB (15658676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cd6b8106895718cb9fdb497c692e1d0d064b7f17763b163bd3d15735190a18`  
		Last Modified: Fri, 13 Oct 2023 01:22:49 GMT  
		Size: 45.0 MB (45011955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19825c9c9402cd7401b6eaa7a91a0bb372c48a36e3aa2825b5cf9869b001c3a`  
		Last Modified: Fri, 13 Oct 2023 01:22:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0aebb2649f8a95566818f1b229bd483da3ad23c119399f0429b53fd6a7f705`  
		Last Modified: Fri, 13 Oct 2023 01:22:40 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca351833ffb8138f715d75b952967bda5fd23c988a405a1838c307adf2b61eb3`  
		Last Modified: Fri, 13 Oct 2023 04:38:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b119416fd62223b19f3b3d2801e0499d4a833928b977f7b11e2941c06c60639`  
		Last Modified: Fri, 13 Oct 2023 04:42:26 GMT  
		Size: 11.4 MB (11377723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54f9ae6da734ed80e24859898241a64b4f5edc4615b3fddf195c4f35fb214e`  
		Last Modified: Fri, 13 Oct 2023 04:42:25 GMT  
		Size: 426.3 KB (426312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe9602942600fd572ccf72a758dd6f47d1b795e84f854fe664561173e0fc37`  
		Last Modified: Fri, 13 Oct 2023 04:42:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:4ecb94e49ee2e518337c8a3fa449bbf2350612c7701771256c78a2728d8efb5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101059844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119b6d80262632b3cb3285815b64f48b3d04b50bd9aa86ac9b21dd9b928ae861`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:05:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:40:58 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:41:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:41:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 22:40:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 22:40:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:40:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 22:40:35 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 22:40:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:40:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:43:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 31 Aug 2023 22:43:33 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 00:30:27 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 00:30:27 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 00:30:27 GMT
COPY dir:41f63d6f5a06b478dc54959857c3543bc5f0d750261384ce2da025f2be358cc8 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:30:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:30:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:30:32 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:30:32 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:30:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d3de389f9fd6a81c60e4d6444266df2002734ab5660161fa9bf374cd8cd473`  
		Last Modified: Tue, 08 Aug 2023 19:44:02 GMT  
		Size: 16.8 MB (16770361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e165ca30b01b3f7117bfc1709d8070e9cee35fb54635d7c6ff96b49f7a43229c`  
		Last Modified: Thu, 31 Aug 2023 20:46:02 GMT  
		Size: 45.2 MB (45190807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c53c5e205160b02aa040b922a9a52180409de51ea851f37b90cc5926f8c75d`  
		Last Modified: Thu, 31 Aug 2023 20:45:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb579eeb6ef00e3901f0af511dd4a4ec2301a5d6f5419709af63f5308a9cde1`  
		Last Modified: Thu, 31 Aug 2023 20:45:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b878f238f00bbbfb3ab8494c2a36d7218b0b88d8f26c9ab8decfeb9e9dbd2d`  
		Last Modified: Thu, 31 Aug 2023 22:49:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9562887bd26d2dbf6489ed6df560f865c3c010051d8c3b1647a5ac14add6db57`  
		Last Modified: Fri, 13 Oct 2023 00:52:01 GMT  
		Size: 11.4 MB (11446474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8255751c3926edbf36879390319e514f6ffd2a882914fad049a6df3bdd56a99`  
		Last Modified: Fri, 13 Oct 2023 00:52:00 GMT  
		Size: 450.4 KB (450419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d506a77875f6250319ba6c55b530e83813696d4d338c4419a4bc8594cd8d3bc1`  
		Last Modified: Fri, 13 Oct 2023 00:52:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:707c8cdb561af2c71bdbca7f6082d35392e527f892e741d0a9a785f71f5fc9ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105767154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad7db33da179a86c58a7ab789d872c1ba7bf3941ece004d9fef240adb47e436`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:44:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:18:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:16:56 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:18:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:18:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:18:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:18:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 21:45:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 21:45:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 21:45:51 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 21:45:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 21:45:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 21:45:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 21:53:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 31 Aug 2023 21:53:49 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 04:15:13 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 04:15:14 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 04:15:15 GMT
COPY dir:9ee85bae6f0f84478128cdbbb1227751230c9b162cb2400ad1decc486cdc3eca in /usr/local/tomcat 
# Fri, 13 Oct 2023 04:15:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:15:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 04:15:26 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 04:15:26 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 04:15:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af03d96af036322b1cf090be8f29d0a3931c623558764bccaca2826ee7b9af6b`  
		Last Modified: Tue, 08 Aug 2023 19:28:27 GMT  
		Size: 18.2 MB (18215568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea89b9045705978ae08dbc08ecc3ba4c6734f0c1e467167b042b988d4a15c6c`  
		Last Modified: Thu, 31 Aug 2023 20:25:52 GMT  
		Size: 42.3 MB (42295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c48daff8a4901abc1dd903b66a1f38c8d07c0503029558c43ac2c292c0f9890`  
		Last Modified: Thu, 31 Aug 2023 20:25:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebfdeda385620ea89f151e01e4707d3e5c29639ef5f820aea977e6b3ca5bf8c`  
		Last Modified: Thu, 31 Aug 2023 20:25:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f072c2ef95c37bca69eadd77eb4e888e04151d43765a6cbc48fefc0c6992c`  
		Last Modified: Thu, 31 Aug 2023 22:03:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a396d388451f63e51786e1c778977b38fe2ff639a50e917e10ad05d60ce35f29`  
		Last Modified: Fri, 13 Oct 2023 04:33:47 GMT  
		Size: 11.5 MB (11472834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02f517a48351ebfb1a44f888f82836f582f4b14ea0b512e72b088a8b29bd2cb`  
		Last Modified: Fri, 13 Oct 2023 04:33:46 GMT  
		Size: 475.2 KB (475205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010f7262e62c1792b0ecf2fc0c7089ba90757e4f33d7620ba05479a9754f86a`  
		Last Modified: Fri, 13 Oct 2023 04:33:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:f07dde14ed77f9cc4df6f3fb873e87e931dac252de514b8a14e1ef522e30f1e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96148136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c5cfc8f8521ac65d7cddd3170fe645a7c836a878b43c71a8209ed56ac89f2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 00:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 00:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:42:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 19:41:50 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 19:42:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 19:42:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 19:42:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 19:42:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:33:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 20:33:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 20:33:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 20:33:07 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 20:33:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 20:33:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 20:36:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 31 Aug 2023 20:36:29 GMT
ENV TOMCAT_MAJOR=8
# Thu, 31 Aug 2023 20:36:29 GMT
ENV TOMCAT_VERSION=8.5.93
# Thu, 31 Aug 2023 20:36:29 GMT
ENV TOMCAT_SHA512=fdd9bd768c2c8b7f57c75f1a4863bd2bde55e8ea7c8b9cb81427ea8be652540bdcb1ff1cd625b9fb0dd48eb750ebef0f0244d12ac574998d5df3a0d339699bcc
# Thu, 31 Aug 2023 20:36:29 GMT
COPY dir:08fdefc50ea37aa9f5a8a87b107050b0684c57739fcdb98c9d49c514c35ce51f in /usr/local/tomcat 
# Thu, 31 Aug 2023 20:36:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:36:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 31 Aug 2023 20:36:35 GMT
EXPOSE 8080
# Thu, 31 Aug 2023 20:36:35 GMT
ENTRYPOINT []
# Thu, 31 Aug 2023 20:36:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:365fa2124eb5f6f369204f3fe0210d9965952628707dfacd4194a8e15caf0420`  
		Last Modified: Thu, 03 Aug 2023 00:03:37 GMT  
		Size: 27.0 MB (27014233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bb71ff7cf2cdfba432549f8f118e2394ed9d63653317801c650fc5cdf556b`  
		Last Modified: Tue, 08 Aug 2023 19:46:12 GMT  
		Size: 16.6 MB (16643421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f8335cbfd803607e4418775211103e787625971a483f5bbcfeb495ff891997`  
		Last Modified: Thu, 31 Aug 2023 19:46:30 GMT  
		Size: 40.6 MB (40631781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee5dd10279f160c205f3da808d80770943d55dd4eb8fff568268221c7742c92`  
		Last Modified: Thu, 31 Aug 2023 19:46:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae7c034ba50796e7495f9e0e35d2d4474e66f5ae7ccd61e8fee054eabd9708e`  
		Last Modified: Thu, 31 Aug 2023 19:46:25 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3b67a3b5e92d2dd02393b7bc8869296dedd641f6433cda55b01b5bb12f6b83`  
		Last Modified: Thu, 31 Aug 2023 20:40:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de02ec31dd056c0263ed1ab98627179a8fbe4850b23600ef40e8b19a202da908`  
		Last Modified: Thu, 31 Aug 2023 20:41:44 GMT  
		Size: 11.4 MB (11406025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd860697ffe99ac673eff645ec5a37b230d1c953d69fd72e46291c728651131a`  
		Last Modified: Thu, 31 Aug 2023 20:41:43 GMT  
		Size: 451.5 KB (451482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ea684d799dbb35fedfed2b82b34ae60533af9b902de44a7a0b4a474d99995`  
		Last Modified: Thu, 31 Aug 2023 20:41:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
