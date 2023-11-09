## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:0ee54bf01f3882bc582f66b3f8e9f8325ce8d90c83af45b9b7d5501dc9d2f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:3398a8a1a9a74ed2d3d86af68cd460d9719efed3d7a7f01116fb07e494c67e42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 MB (599658137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec64dc2e25fd8ff4e90b5830a155559b39a3332e0f0d877c569bf69c4e00362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:51:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:27:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:44 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:29:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:29:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:29:19 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:29:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 03:37:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:37:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 03:37:14 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 03:37:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:37:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:39:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 03:39:32 GMT
ENV TOMCAT_MAJOR=9
# Tue, 31 Oct 2023 03:39:32 GMT
ENV TOMCAT_VERSION=9.0.82
# Tue, 31 Oct 2023 03:39:32 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Tue, 31 Oct 2023 03:39:33 GMT
COPY dir:4fdd96615cb958335f3b12700d702e3ffcee07613ee616e5456e799e6dfe0b52 in /usr/local/tomcat 
# Tue, 31 Oct 2023 03:39:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:39:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Oct 2023 03:39:39 GMT
EXPOSE 8080
# Tue, 31 Oct 2023 03:39:39 GMT
ENTRYPOINT []
# Tue, 31 Oct 2023 03:39:39 GMT
CMD ["catalina.sh" "run"]
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 09 Nov 2023 20:22:33 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 09 Nov 2023 20:25:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 09 Nov 2023 20:25:40 GMT
ENV XWIKI_VERSION=14.10.19
# Thu, 09 Nov 2023 20:25:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.19
# Thu, 09 Nov 2023 20:25:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=14b88314f9af3c122e3329d13ad2a8a473a774fa1bc8b5b96d08bbf36e56c453
# Thu, 09 Nov 2023 20:26:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 09 Nov 2023 20:26:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 09 Nov 2023 20:26:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 09 Nov 2023 20:26:24 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 09 Nov 2023 20:26:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 09 Nov 2023 20:26:25 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 09 Nov 2023 20:26:25 GMT
VOLUME [/usr/local/xwiki]
# Thu, 09 Nov 2023 20:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:26:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4452d37e1e46888f8dbbf8283d09e03f1bec00021532334441fe00c95aa8b15`  
		Last Modified: Mon, 30 Oct 2023 23:36:06 GMT  
		Size: 17.5 MB (17454768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae6cc00f059e812c753a4a45b4a388d14bb714a104ec8b33c31436807f31055`  
		Last Modified: Mon, 30 Oct 2023 23:37:50 GMT  
		Size: 47.1 MB (47149391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaec5da5e638ca5d7247c8697d0721bdac4826945748d0239718f23f657abc5`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7dcc43773c1bcab928db7ca63abd5a20c525148ae1b63c03bfdcdef7e03153`  
		Last Modified: Mon, 30 Oct 2023 23:37:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6729bb2516f9ee1f23d3c6b1a60b651eb413c43b62cdc554de84df2590085216`  
		Last Modified: Tue, 31 Oct 2023 03:53:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9168864721356533b0669f4446b3b9f62f971b648862ea49c25c758117374986`  
		Last Modified: Tue, 31 Oct 2023 03:56:21 GMT  
		Size: 12.3 MB (12315466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541fb3b6d3fc04d699b424c3d27f1fd761b49c3a2f8635c10bfc6950d3504c5a`  
		Last Modified: Tue, 31 Oct 2023 03:56:21 GMT  
		Size: 3.0 MB (2970840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333283eafa5961340497c34e61f546f2485c7097991f05509d2f7c8b1709e357`  
		Last Modified: Tue, 31 Oct 2023 03:56:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3405174303cd4fae8bb04b4cf66ed174068ab0084eb76a3d84bf90cbef831b1`  
		Last Modified: Thu, 09 Nov 2023 20:28:42 GMT  
		Size: 179.3 MB (179298682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33930095015d20830167fc4c7e48748304b5f63c9fad78767fcbbad32fb2cef`  
		Last Modified: Thu, 09 Nov 2023 20:28:35 GMT  
		Size: 309.1 MB (309079593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ff1097fd161adeaa952d049da401f872cde5b2280eae813a6ecde4ecbbfe75`  
		Last Modified: Thu, 09 Nov 2023 20:28:18 GMT  
		Size: 936.8 KB (936847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985902aecb3809ac52ddb29d175a793e66c999b509e29af022c749d088916627`  
		Last Modified: Thu, 09 Nov 2023 20:28:18 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a462bb1792f534598c81f714fa261bfe3c82538c68a3b29937865baaf15f46`  
		Last Modified: Thu, 09 Nov 2023 20:28:18 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d08be39e2b7f3d083d17c894896bbdd0189f1a5a682ad43e20b5276b7c8a7cf`  
		Last Modified: Thu, 09 Nov 2023 20:28:18 GMT  
		Size: 6.0 KB (6011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e544e7b94f639d3045243db21c033c00f5e3190d7203bdde32c795cefaf3e6`  
		Last Modified: Thu, 09 Nov 2023 20:28:18 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4c324bb427d5dabb1e575b323c28d1d581653d350866d446eb40fa6ee82e3092
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.1 MB (586125027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d78d216dbb381b1009c9ae94f4cd81b81adbeb5a875fe922924dbd3a6d9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:41:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:41:33 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Mon, 30 Oct 2023 23:43:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:43:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:43:01 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:43:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 02:56:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 02:56:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 02:56:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 02:56:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 02:56:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:56:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:00:06 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 31 Oct 2023 03:00:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 31 Oct 2023 03:00:06 GMT
ENV TOMCAT_VERSION=9.0.82
# Tue, 31 Oct 2023 03:00:06 GMT
ENV TOMCAT_SHA512=2b13f11f4e0d0b9aee667c256c6ea5d2853b067e8b7e8293f117da050d3833fda8aa9d9ad278bd12fb7fbf0825108c7d0384509f44c05f9bad73eb099cfaa128
# Tue, 31 Oct 2023 03:00:06 GMT
COPY dir:8754492acebcfe4fe04b0583bac4d3d93afaa6139254eaf140e87831c5de5fae in /usr/local/tomcat 
# Tue, 31 Oct 2023 03:00:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 03:00:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Oct 2023 03:00:11 GMT
EXPOSE 8080
# Tue, 31 Oct 2023 03:00:11 GMT
ENTRYPOINT []
# Tue, 31 Oct 2023 03:00:11 GMT
CMD ["catalina.sh" "run"]
# Tue, 31 Oct 2023 04:24:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 31 Oct 2023 04:24:29 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 31 Oct 2023 04:24:29 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 31 Oct 2023 04:24:29 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 31 Oct 2023 04:24:29 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 31 Oct 2023 04:24:29 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 31 Oct 2023 04:28:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 04:30:16 GMT
ENV XWIKI_VERSION=14.10.18
# Tue, 31 Oct 2023 04:30:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.18
# Tue, 31 Oct 2023 04:30:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=66209b2e457b1b14b177f1f4918be37c2ae65c6655d16b314db6c52cc37003ff
# Tue, 31 Oct 2023 04:30:57 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 31 Oct 2023 04:31:00 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 31 Oct 2023 04:31:00 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 06 Nov 2023 23:54:57 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 06 Nov 2023 23:54:57 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 06 Nov 2023 23:54:57 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 06 Nov 2023 23:54:58 GMT
VOLUME [/usr/local/xwiki]
# Mon, 06 Nov 2023 23:54:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Nov 2023 23:54:58 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035bfa3ea28e4a939fa769d2862227b94b4b5b961f65ac5df2ea3df7a0c51e4`  
		Last Modified: Mon, 30 Oct 2023 23:48:25 GMT  
		Size: 12.8 MB (12843579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44426d62154b920edc46b4f9c3d95ead5cff773239ebb0640ed78a3eabd75d3d`  
		Last Modified: Mon, 30 Oct 2023 23:49:42 GMT  
		Size: 45.4 MB (45399290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b0a8b8196635efd1dce5dd763022df6a147662cd3aa1dcff312442551fce3d`  
		Last Modified: Mon, 30 Oct 2023 23:49:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeea1065ab43308ab77465a15be2c3e434488174fb1da412ee0e1f868c0ea93`  
		Last Modified: Mon, 30 Oct 2023 23:49:37 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f94ea910cb3af1fe712475caf27c4ff01461027655150f4c642120033d2267`  
		Last Modified: Tue, 31 Oct 2023 03:10:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a8008513efd39a0f4ccee25576aba434caaac1336e6f5de140e6e098c06e61`  
		Last Modified: Tue, 31 Oct 2023 03:14:04 GMT  
		Size: 12.3 MB (12323862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d1140858fb04f2435d7c00d473576f8aa86d828d1746d2c7a1cd2db4ff68e2`  
		Last Modified: Tue, 31 Oct 2023 03:14:03 GMT  
		Size: 2.8 MB (2810137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24a2f4303583c442267a0085b344ca1c142e3c1002b540c0661244a397ec58`  
		Last Modified: Tue, 31 Oct 2023 03:14:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916479ef3f5430044e711b7aeaed2061664dd26c0804d18806385735439eac1`  
		Last Modified: Tue, 31 Oct 2023 04:34:29 GMT  
		Size: 174.3 MB (174333074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebd4b3f8580093990fe9cf603aa9901d6500d2d16e6df04f959ee0a707e596`  
		Last Modified: Tue, 31 Oct 2023 04:36:12 GMT  
		Size: 309.1 MB (309072843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aa38fc992a048487aafd63ce2ce4a1e24427eaa8056b3a8364e6284f475e09`  
		Last Modified: Tue, 31 Oct 2023 04:35:55 GMT  
		Size: 936.9 KB (936853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0c5c77e77f33f930fea284861cbe09e835a4e5aa40d593b649912c3c5a60fc`  
		Last Modified: Tue, 31 Oct 2023 04:35:55 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21c20426e17ed1545702d147f23bcab5953c97fa9476eb49b9d7eab2d7a3971`  
		Last Modified: Mon, 06 Nov 2023 23:57:32 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c277cc218c923ef1e06cc724ab20efc812b6eb277ac4eed30c4280127314f`  
		Last Modified: Mon, 06 Nov 2023 23:57:32 GMT  
		Size: 6.0 KB (6021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce45e63b0186c5a06ecd1805193f0171b51e99125be5f12942bf103222be6a0`  
		Last Modified: Mon, 06 Nov 2023 23:57:32 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
