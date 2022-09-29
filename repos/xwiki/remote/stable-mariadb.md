## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:2b4db037c3cce61655671668248c9f10bc8369c1b13e7f0c2ca4c6089a782459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:843d1ba6a88f6c64892ef5ee774f6e2ebb2fdb7847e71d7839172ee6e35b8081
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.4 MB (585423379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8bcd465501daf41dd6162cbdc612fd0e2600b429922a4e1be1f5a43349ce48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:22:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:22:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:32 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:24:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:35:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 10:35:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:35:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 10:35:59 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 10:35:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:35:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:43:14 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 10:43:14 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 00:57:08 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 00:57:08 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 00:57:09 GMT
COPY dir:c2d17f009b107041d4d17d92bf36c16fe4bdbe0a066210c1fff3476a1bbce66a in /usr/local/tomcat 
# Tue, 27 Sep 2022 00:57:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 00:57:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 00:57:14 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 00:57:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 27 Sep 2022 01:49:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 27 Sep 2022 01:49:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 27 Sep 2022 01:49:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 27 Sep 2022 01:49:05 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 27 Sep 2022 01:49:05 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 27 Sep 2022 01:49:05 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 27 Sep 2022 02:11:57 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 29 Sep 2022 19:31:57 GMT
ENV XWIKI_VERSION=14.8
# Thu, 29 Sep 2022 19:31:57 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.8
# Thu, 29 Sep 2022 19:31:57 GMT
ENV XWIKI_DOWNLOAD_SHA256=87d2ffb0c5c179fe854e92b52707ee2a147d588b0fdf1bb0945657ce27163356
# Thu, 29 Sep 2022 19:32:37 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 29 Sep 2022 19:33:34 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Thu, 29 Sep 2022 19:33:34 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Thu, 29 Sep 2022 19:33:34 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Thu, 29 Sep 2022 19:33:34 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Thu, 29 Sep 2022 19:33:34 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Thu, 29 Sep 2022 19:33:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 29 Sep 2022 19:33:35 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 29 Sep 2022 19:33:35 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 29 Sep 2022 19:33:36 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 29 Sep 2022 19:33:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 29 Sep 2022 19:33:36 GMT
VOLUME [/usr/local/xwiki]
# Thu, 29 Sep 2022 19:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 19:33:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca45fc4c4ca4ea0526871f8fe0527c23dbb2d24df2aff307d5b41e7b5ebc3fe`  
		Last Modified: Fri, 02 Sep 2022 05:28:37 GMT  
		Size: 12.4 MB (12441851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522d9aa14d93cbdfa4eac0048d607d396eea10c1bfe2da9eafd0ee8b562d5c45`  
		Last Modified: Fri, 02 Sep 2022 05:30:43 GMT  
		Size: 46.5 MB (46498618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a19e0a4285757e7a688613e8c01972397948c470b96c5e1a9eef9c1acb847e3`  
		Last Modified: Fri, 02 Sep 2022 05:30:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee310b06f35a03f98596c215dcbed87e02dc080494393a5b0a49ad322f2cd5`  
		Last Modified: Fri, 02 Sep 2022 10:57:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e8a1fed1bb15c88c9b50f6f56b3fb068fce56810045b90a1a23ab1dfbd217c`  
		Last Modified: Tue, 27 Sep 2022 01:12:43 GMT  
		Size: 12.2 MB (12190892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523b60b0c7741f5b434421cc4bee6e30a66b1b7d00cb6a10a5afa553ca7888c`  
		Last Modified: Tue, 27 Sep 2022 01:12:42 GMT  
		Size: 452.3 KB (452255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374839c290543def0c2cdbddc5b8b450a5da48ce950d19d51a609a3f6557d18`  
		Last Modified: Tue, 27 Sep 2022 01:12:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0eab7cc2054aac3ca7537d37b7b0622a868a576da87c7ea70b3722f33fb16bc`  
		Last Modified: Tue, 27 Sep 2022 02:18:52 GMT  
		Size: 178.3 MB (178317499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcfd19ccd4ddf9532350c1a03de680e9be6f4d2027a0d2f42502f22a4c788a3`  
		Last Modified: Thu, 29 Sep 2022 19:34:57 GMT  
		Size: 304.5 MB (304539103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce172fdfba93e55944c63c1242336d95cedccc824e9146273b8fd7f7389d757`  
		Last Modified: Thu, 29 Sep 2022 19:36:15 GMT  
		Size: 543.9 KB (543934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020fc303d39329c8263e834209c55ed83a710adb2ee197251b887c3f70f0cfa0`  
		Last Modified: Thu, 29 Sep 2022 19:36:15 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cf3d7ca27d21fc95826bfa39e745271ad3a2d84449b78cf08530ea60a8762a`  
		Last Modified: Thu, 29 Sep 2022 19:36:15 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0720ea53601850c55ce990110165587c05534fec7bea70c00fbfa57783f8a8`  
		Last Modified: Thu, 29 Sep 2022 19:36:15 GMT  
		Size: 5.9 KB (5892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2193e7ca5727cd6d34acb819eb41007bc190e82e2b4b07ad30fb665a5f15b058`  
		Last Modified: Thu, 29 Sep 2022 19:36:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:3f9296ea16d6d1d9ac5b0e9c0f4f6eb02507b1ff86edf04834986c7a2323f724
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.4 MB (576443108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3602cd3c8dda7bc403e5eccfde602fb92d3f6d33b9c65d236e22acd8dbc7c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:56:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:56:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:56:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:37 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:58:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:58:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 09:16:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 09:16:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 09:16:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 09:16:17 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 09:16:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:16:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:28:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 09:28:21 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 01:14:44 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 01:14:44 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 01:14:46 GMT
COPY dir:57bdf8d728fbf44b85e79da567d6be1467ce1d7fb2333d3921d41977d45df4db in /usr/local/tomcat 
# Tue, 27 Sep 2022 01:14:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 01:14:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 01:14:55 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 01:14:56 GMT
CMD ["catalina.sh" "run"]
# Tue, 27 Sep 2022 02:00:50 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 27 Sep 2022 02:00:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 27 Sep 2022 02:00:52 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 27 Sep 2022 02:00:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 27 Sep 2022 02:00:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 27 Sep 2022 02:00:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 27 Sep 2022 02:01:37 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 29 Sep 2022 21:51:02 GMT
ENV XWIKI_VERSION=14.8
# Thu, 29 Sep 2022 21:51:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.8
# Thu, 29 Sep 2022 21:51:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=87d2ffb0c5c179fe854e92b52707ee2a147d588b0fdf1bb0945657ce27163356
# Thu, 29 Sep 2022 21:51:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 29 Sep 2022 21:53:15 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Thu, 29 Sep 2022 21:53:16 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Thu, 29 Sep 2022 21:53:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Thu, 29 Sep 2022 21:53:17 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Thu, 29 Sep 2022 21:53:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Thu, 29 Sep 2022 21:53:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 29 Sep 2022 21:53:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 29 Sep 2022 21:53:22 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 29 Sep 2022 21:53:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 29 Sep 2022 21:53:24 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 29 Sep 2022 21:53:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 29 Sep 2022 21:53:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:53:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb549d469a383cfda4a1db7a2dd57a269b1b7a2325cbf0e9d8f5c604a72eed`  
		Last Modified: Fri, 02 Sep 2022 05:04:20 GMT  
		Size: 12.4 MB (12397459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e2de83fd0832584ab1379ffe8c12ed166b2406e60b5e297487e5df856f4c9`  
		Last Modified: Fri, 02 Sep 2022 05:07:00 GMT  
		Size: 44.8 MB (44824448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3970fa7bb851d635c04498eaedd0112cf0274c4b699bb547b26e4538cb06b5`  
		Last Modified: Fri, 02 Sep 2022 05:06:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c016dc02a28329c1d799871b3ae0d29c9cf580c2ad6e371006e19b93bb7eb80`  
		Last Modified: Fri, 02 Sep 2022 09:52:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457d0aeb8ff8fc5f8b53e2586c2367d5f0918820b7e83c0e8131e03cb6c39aca`  
		Last Modified: Tue, 27 Sep 2022 01:35:50 GMT  
		Size: 12.2 MB (12198613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a67b68994e3cd774a174145d0ddaf9ffb8fa73f2ea7a6c402d6ea5c883eb520`  
		Last Modified: Tue, 27 Sep 2022 01:35:49 GMT  
		Size: 214.2 KB (214199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e07edb12837df6f02c95929c5e37f0ddb4401550321bd3c423180a1a260eaea`  
		Last Modified: Tue, 27 Sep 2022 02:11:16 GMT  
		Size: 173.3 MB (173331755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e90f36fe0a5c818dd09d2735c4d89502d37bc8d8cc28c8d089b131b766bbfc`  
		Last Modified: Thu, 29 Sep 2022 21:55:52 GMT  
		Size: 304.5 MB (304539013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6e5944af10f783d562d9f7f27d41162b8a691a92d6014dee8b8adc4ec37315`  
		Last Modified: Thu, 29 Sep 2022 21:57:26 GMT  
		Size: 543.9 KB (543934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0efd39804beebca3cd72017fb4fe8ce5699eaf0fb3345cedb0f6150e9df297`  
		Last Modified: Thu, 29 Sep 2022 21:57:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a48862727a19215dfdbdb4dd027852e18155ebe17f8adbfaa6a362ea30b3b36`  
		Last Modified: Thu, 29 Sep 2022 21:57:26 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1072f96e676f0a7ea8819bc8cb8c646248cc9bfae913d03bca7175382221e08`  
		Last Modified: Thu, 29 Sep 2022 21:57:26 GMT  
		Size: 5.9 KB (5890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8e7911cbe13ac990da1cd6b871b31e6c058456a7fb09cb8e075200730b716`  
		Last Modified: Thu, 29 Sep 2022 21:57:26 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
