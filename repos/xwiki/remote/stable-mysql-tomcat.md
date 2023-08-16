## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:b20cce284f537bcd3940d6e6cd36e0e84a732ac646bc0d540c9e45c2defda57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:fd1b3769fb9880718ae47a7aa68151b3409d7c955ac6ca962b92d47f1936f5ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592003995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc47cfc5c6ce58e590bd76221dd5e2fd4a57dd23e3cfc84282548fefd4899c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Tue, 08 Aug 2023 19:21:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:22:14 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:22:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:10:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:10:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 21:52:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 21:52:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 21:52:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 21:52:07 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 21:52:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 21:52:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 21:54:45 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 14 Aug 2023 21:54:45 GMT
ENV TOMCAT_MAJOR=9
# Tue, 15 Aug 2023 23:53:06 GMT
ENV TOMCAT_VERSION=9.0.79
# Tue, 15 Aug 2023 23:53:06 GMT
ENV TOMCAT_SHA512=7a0d99b5fc37c9e9ac26b554fab9147ce0a2ba59fad41e2565b15e9f6e137bf0105f5c9cd6b7b508837ff24feb7b95b2aba49e0abc7b1480a30a11606e79802a
# Tue, 15 Aug 2023 23:53:06 GMT
COPY dir:6f743858da11a33bdbf66b0d26c80e2e6d26924582bd363d63e06591d3c36edf in /usr/local/tomcat 
# Tue, 15 Aug 2023 23:53:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Aug 2023 23:53:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 15 Aug 2023 23:53:12 GMT
EXPOSE 8080
# Tue, 15 Aug 2023 23:53:13 GMT
ENTRYPOINT []
# Tue, 15 Aug 2023 23:53:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 16 Aug 2023 00:46:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 16 Aug 2023 00:47:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:47:50 GMT
ENV XWIKI_VERSION=15.6
# Wed, 16 Aug 2023 00:47:50 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.6
# Wed, 16 Aug 2023 00:47:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=024f0f2d5c4dbc5bdad00f2dca260a5aad5cd820812b3ba6088a730cbe4f84cd
# Wed, 16 Aug 2023 00:48:30 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 16 Aug 2023 00:48:31 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 16 Aug 2023 00:48:31 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 16 Aug 2023 00:48:31 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 16 Aug 2023 00:48:31 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 16 Aug 2023 00:48:31 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 16 Aug 2023 00:48:32 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 16 Aug 2023 00:48:32 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 16 Aug 2023 00:48:32 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 16 Aug 2023 00:48:33 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 16 Aug 2023 00:48:33 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 16 Aug 2023 00:48:33 GMT
VOLUME [/usr/local/xwiki]
# Wed, 16 Aug 2023 00:48:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 00:48:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d9603a2223f0c0337b5489031adc59113c119d64dfce6852f6114f42f2f05`  
		Last Modified: Tue, 08 Aug 2023 19:27:08 GMT  
		Size: 12.9 MB (12902861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ec547f8ce2155ce58a25da4ddaaffb94bbba064f0491bbc9535447779218de`  
		Last Modified: Tue, 08 Aug 2023 19:30:50 GMT  
		Size: 46.9 MB (46864855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c96886bebf4fd42e9a6622257a11b02a6c388c2a8b5dda93d1087b4f6ee1fd`  
		Last Modified: Tue, 08 Aug 2023 19:30:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5de702898874688381ecd4779b9d0d8df8abdccef888811fc78321518172b1`  
		Last Modified: Mon, 14 Aug 2023 18:16:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e50d0a3807cd97b9be2cc76eba12dc36e698a4ffe4bec31525a059e18dbecf`  
		Last Modified: Mon, 14 Aug 2023 22:06:39 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180ed73b716305f4ab8ee7b328da57f5cf3c7be8e4064c0704925dad21c8d9e`  
		Last Modified: Wed, 16 Aug 2023 00:17:10 GMT  
		Size: 12.3 MB (12284413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d5833e5dd88f8a353e1a9b06a48ddad875d3c5bd15a9e03450629cb2a6471b`  
		Last Modified: Wed, 16 Aug 2023 00:17:10 GMT  
		Size: 455.7 KB (455659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eebd6c1818daa4bde850d749d0614c1f52cd81f539a5ab75d75f3474b770f75`  
		Last Modified: Wed, 16 Aug 2023 00:17:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504d73c0b8ad00c7eab1a6eae57ee9ed30edadadc6d0c6b1e4b2bc11f6c4ea6e`  
		Last Modified: Wed, 16 Aug 2023 00:54:36 GMT  
		Size: 178.4 MB (178356670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd13ea2a3ad2a9e2a62e9f9913b6d1ac4a12144d2122a6c67b147b9a826227d1`  
		Last Modified: Wed, 16 Aug 2023 00:54:32 GMT  
		Size: 308.4 MB (308350977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c884aa53d7a3c61d1bb0a9622b02b4ca84288f12c83fc9e331130de0923303f`  
		Last Modified: Wed, 16 Aug 2023 00:54:12 GMT  
		Size: 2.3 MB (2343674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb63458ea061fa9df11590ae4289250ab1502c33ce93376ed61a84100c07a85`  
		Last Modified: Wed, 16 Aug 2023 00:54:11 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2be1f55f0b3a5ecddcc0eeb625445886133a3be47d4a317dac723c3a890d41`  
		Last Modified: Wed, 16 Aug 2023 00:54:11 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be92a84cc6e169b4693f809edcc75bb056c06c8a59d96f357c32850765cb6639`  
		Last Modified: Wed, 16 Aug 2023 00:54:11 GMT  
		Size: 6.3 KB (6300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a03e52303df1302e46fa26c48015adb44cc8791af26acca0f1d963ab9bebfc`  
		Last Modified: Wed, 16 Aug 2023 00:54:11 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:689dc6f28d53d6142bb4c2c27e433707589f83643805a4a34afa6d17b1bd3aa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583276122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221c3c8462c660be1a801fdeab56dae75b577fecfc9cc8b5afe086833868b928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Tue, 08 Aug 2023 19:40:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:41:25 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:41:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:41:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 20:04:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 20:04:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 20:04:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 20:04:29 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 20:04:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 20:04:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 20:07:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 14 Aug 2023 20:07:00 GMT
ENV TOMCAT_MAJOR=9
# Wed, 16 Aug 2023 00:35:21 GMT
ENV TOMCAT_VERSION=9.0.79
# Wed, 16 Aug 2023 00:35:21 GMT
ENV TOMCAT_SHA512=7a0d99b5fc37c9e9ac26b554fab9147ce0a2ba59fad41e2565b15e9f6e137bf0105f5c9cd6b7b508837ff24feb7b95b2aba49e0abc7b1480a30a11606e79802a
# Wed, 16 Aug 2023 00:35:21 GMT
COPY dir:461066496d26dd5a5828a92d39452ffdbbeb779430a254646dcd0c272ba9762e in /usr/local/tomcat 
# Wed, 16 Aug 2023 00:35:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:35:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 16 Aug 2023 00:35:26 GMT
EXPOSE 8080
# Wed, 16 Aug 2023 00:35:26 GMT
ENTRYPOINT []
# Wed, 16 Aug 2023 00:35:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 16 Aug 2023 14:01:36 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 16 Aug 2023 14:04:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:04:15 GMT
ENV XWIKI_VERSION=15.6
# Wed, 16 Aug 2023 14:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.6
# Wed, 16 Aug 2023 14:04:15 GMT
ENV XWIKI_DOWNLOAD_SHA256=024f0f2d5c4dbc5bdad00f2dca260a5aad5cd820812b3ba6088a730cbe4f84cd
# Wed, 16 Aug 2023 14:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 16 Aug 2023 14:04:58 GMT
ENV MYSQL_JDBC_VERSION=8.0.33
# Wed, 16 Aug 2023 14:04:58 GMT
ENV MYSQL_JDBC_SHA256=e2a3b2fc726a1ac64e998585db86b30fa8bf3f706195b78bb77c5f99bf877bd9
# Wed, 16 Aug 2023 14:04:58 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.0.33
# Wed, 16 Aug 2023 14:04:58 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.0.33.jar
# Wed, 16 Aug 2023 14:04:58 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.0.33.jar
# Wed, 16 Aug 2023 14:04:59 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 16 Aug 2023 14:04:59 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 16 Aug 2023 14:04:59 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 16 Aug 2023 14:05:00 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 16 Aug 2023 14:05:00 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 16 Aug 2023 14:05:00 GMT
VOLUME [/usr/local/xwiki]
# Wed, 16 Aug 2023 14:05:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 14:05:00 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91712d801b234a271df55fd60b35e7d2918ce5ae0fb7ce56a8de0edb8151fd0e`  
		Last Modified: Tue, 08 Aug 2023 19:44:21 GMT  
		Size: 12.8 MB (12844180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aeb71c3e8ddfbdbcdf7f366fa14814e5ae4bc3c34c81ee51cd629b818bbedac`  
		Last Modified: Tue, 08 Aug 2023 19:46:59 GMT  
		Size: 45.2 MB (45190380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29f50935a8980aae448b158b40171ce38beb0eaaac6885c4f54cce54e91111d`  
		Last Modified: Tue, 08 Aug 2023 19:46:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2bfbde8872df971f3dccf01060b0d0c7b10d21fd75574bdb1dabba083f45d3`  
		Last Modified: Mon, 14 Aug 2023 18:12:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ed8887270373776416bdecd9528b66f3f8efcb02d4b8b41d880ea9b7a7e432`  
		Last Modified: Mon, 14 Aug 2023 20:17:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f098a2fb0f675045614bc3c30371ad172f61e687cef29ae96f8f0f479268bf`  
		Last Modified: Wed, 16 Aug 2023 00:55:31 GMT  
		Size: 12.3 MB (12290930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce284ea3552cfa56ab55b30846cfb330be57911c69f7f8d31584fc370de52bc0`  
		Last Modified: Wed, 16 Aug 2023 00:55:30 GMT  
		Size: 456.0 KB (455963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7906e8039a57f4dfb0e5b9431d701fc47991feb1aeaafe92fef9017945e7e2f4`  
		Last Modified: Wed, 16 Aug 2023 00:55:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe327fa601dc7fb8a948046dc903da9a7e7dfe9c361f98cfb8c9f8dc22e0440`  
		Last Modified: Wed, 16 Aug 2023 14:10:48 GMT  
		Size: 173.4 MB (173395364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11f07e0a888880786cd8eba51acfa2d4ceeac1c8031e509b2f49e1f12eb6296`  
		Last Modified: Wed, 16 Aug 2023 14:10:51 GMT  
		Size: 308.4 MB (308350978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03927e8835894d1bb8f8cc5f966c39f7f56bc2cc074a6b269de399f2d4adcff1`  
		Last Modified: Wed, 16 Aug 2023 14:10:29 GMT  
		Size: 2.3 MB (2343670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4e34bb57e80924d53751fb5048d438b008ca4546ffc296650ca2f7442d2b58`  
		Last Modified: Wed, 16 Aug 2023 14:10:29 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347225e5e7287a0fc1be74947b13f91c675265cc321f4710328eaa9d6620c560`  
		Last Modified: Wed, 16 Aug 2023 14:10:29 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca068abc5101f9ac7bc12c0e66817ad276db7f48ff8b07dacdb2d8989f7e775`  
		Last Modified: Wed, 16 Aug 2023 14:10:29 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f5437c642b02a44652081bcdeefbe7188200bb26f114d2d14947117164240`  
		Last Modified: Wed, 16 Aug 2023 14:10:29 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
