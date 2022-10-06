## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:083051fc11c82a234d9f4b53914c683c590632c352fc210f01d427dee1d635f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2326751a184014a0cfc56a04a50d0a4ab3307dcecbae397ffeff1288306e4006
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573563677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e812d0db972383b87ea190c7b5f2fa01ea86fd7fe93e0f6d0441558ce6b6a739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:20 GMT
ADD file:6cd2e13356aa5339c1f2abd3c210a52f6ed74fae05cd61aa09f37b6a4764f65c in / 
# Tue, 04 Oct 2022 23:35:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 16:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 16:59:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 17:00:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:01:31 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 05 Oct 2022 17:02:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 17:02:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 06 Oct 2022 05:18:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Oct 2022 05:18:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 05:18:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 06 Oct 2022 05:18:33 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Oct 2022 05:18:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 05:18:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 05:25:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Oct 2022 05:25:51 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Oct 2022 05:25:51 GMT
ENV TOMCAT_VERSION=9.0.67
# Thu, 06 Oct 2022 05:25:51 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Thu, 06 Oct 2022 05:25:52 GMT
COPY dir:71543b1840afeb5fff91a5da9a1094db2260bfc1f55af9f696c13a40a6fdafd7 in /usr/local/tomcat 
# Thu, 06 Oct 2022 05:25:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:25:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 06 Oct 2022 05:25:57 GMT
EXPOSE 8080
# Thu, 06 Oct 2022 05:25:57 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Oct 2022 09:41:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 06 Oct 2022 09:41:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 06 Oct 2022 09:41:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 06 Oct 2022 09:41:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 06 Oct 2022 09:41:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 06 Oct 2022 09:41:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 06 Oct 2022 09:42:56 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 09:47:01 GMT
ENV XWIKI_VERSION=13.10.9
# Thu, 06 Oct 2022 09:47:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.9
# Thu, 06 Oct 2022 09:47:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=ad57639016b1bfd1cdf84de764b310a65416832645c6bbfd933ec26fd977bb6a
# Thu, 06 Oct 2022 09:47:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 06 Oct 2022 09:48:38 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Thu, 06 Oct 2022 09:48:38 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Thu, 06 Oct 2022 09:48:38 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Thu, 06 Oct 2022 09:48:38 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Thu, 06 Oct 2022 09:48:38 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Thu, 06 Oct 2022 09:48:39 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 06 Oct 2022 09:48:39 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 06 Oct 2022 09:48:39 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 06 Oct 2022 09:48:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 06 Oct 2022 09:48:40 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 06 Oct 2022 09:48:40 GMT
VOLUME [/usr/local/xwiki]
# Thu, 06 Oct 2022 09:48:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 09:48:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cf92e523b49ea3d1fae59f5f082437a5f96c244fda6697995920142ff31d59cf`  
		Last Modified: Tue, 04 Oct 2022 03:04:01 GMT  
		Size: 30.4 MB (30428928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4c7f172af2471a1945e9feb3dab4254026b8c38f20c75ae781436a4495e6db`  
		Last Modified: Wed, 05 Oct 2022 17:07:10 GMT  
		Size: 12.4 MB (12442343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521599bc479fb2b0da911ac0f7237ba1dd87823d0d2b609de333aef4766022a0`  
		Last Modified: Wed, 05 Oct 2022 17:09:25 GMT  
		Size: 46.5 MB (46498622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd90861fe76e553b9447451baf69d735ce869c254ee2968b0e893c35bd7a38`  
		Last Modified: Wed, 05 Oct 2022 17:09:19 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba416a4250746409b3c6db8225e8a0b0e59fcac990b18d4e524f989705055f9`  
		Last Modified: Thu, 06 Oct 2022 05:39:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751aac03990e4ea8e82c6c834dc6de5a5f007dc4b545807f7cb9dc60b9dcde75`  
		Last Modified: Thu, 06 Oct 2022 05:45:45 GMT  
		Size: 12.2 MB (12190879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a633b09ed6004bcd8c31ee267fedbbe19458a6ae19db042cab6b0af9e448ed`  
		Last Modified: Thu, 06 Oct 2022 05:45:44 GMT  
		Size: 452.6 KB (452634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e88918333520953ec800adb39c81d66a0ccc5ef5caea7e37866cd22c59ab46`  
		Last Modified: Thu, 06 Oct 2022 05:45:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223d712a4579a8b61296eae4606e79bdb8bef19764ad8475d630e70be02b417`  
		Last Modified: Thu, 06 Oct 2022 09:49:58 GMT  
		Size: 178.3 MB (178318669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd5063434d87152ad129d0bb986fb779b083caf87c19f306bc559520bff24df`  
		Last Modified: Thu, 06 Oct 2022 09:53:18 GMT  
		Size: 292.7 MB (292675713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ef46148d75f1a124d1bf9858106ddf55c699a41b3c2cc2f0b8a3c4865099a`  
		Last Modified: Thu, 06 Oct 2022 09:54:28 GMT  
		Size: 543.9 KB (543935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f741d33236cbaa7323acf393a3858a700b77b6664e6ed4dad50080cc4662cc`  
		Last Modified: Thu, 06 Oct 2022 09:54:27 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de87752c68d1f37019229e1d62809d22fa79b61eadc3bacb37b016e432f06ba5`  
		Last Modified: Thu, 06 Oct 2022 09:54:27 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f4cbbffaef2cae96753478c011656d271c461ba61ea6923eecffadbe203bb`  
		Last Modified: Thu, 06 Oct 2022 09:54:27 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9c8142a23697b4f88d5ec37c5d8b96b2ad4af75d73dd029cf3def2ffabcff8`  
		Last Modified: Thu, 06 Oct 2022 09:54:27 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d451f1ce20ee28eb729b59a700fab9659279f6f908f6ffd2cab47c7f1a31d87d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564581244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3775cc9456cf96ae5c23086b0b544d3f993b04f7cfdd93bb134f8870d09c5b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 15:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 15:44:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 15:44:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 15:44:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 15:45:34 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 05 Oct 2022 15:46:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 15:46:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 06 Oct 2022 04:22:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 06 Oct 2022 04:22:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 04:22:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 06 Oct 2022 04:22:58 GMT
WORKDIR /usr/local/tomcat
# Thu, 06 Oct 2022 04:22:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 04:23:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 06 Oct 2022 04:34:36 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 06 Oct 2022 04:34:36 GMT
ENV TOMCAT_MAJOR=9
# Thu, 06 Oct 2022 04:34:37 GMT
ENV TOMCAT_VERSION=9.0.67
# Thu, 06 Oct 2022 04:34:38 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Thu, 06 Oct 2022 04:34:40 GMT
COPY dir:e620d94d416a41ca4953387c2d652cc2f2381fff346f413f70cd2e9d6aafaed3 in /usr/local/tomcat 
# Thu, 06 Oct 2022 04:34:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 04:34:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 06 Oct 2022 04:34:49 GMT
EXPOSE 8080
# Thu, 06 Oct 2022 04:34:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 06 Oct 2022 08:11:52 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 06 Oct 2022 08:11:52 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 06 Oct 2022 08:11:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 06 Oct 2022 08:11:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 06 Oct 2022 08:11:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 06 Oct 2022 08:11:56 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 06 Oct 2022 08:12:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 08:18:36 GMT
ENV XWIKI_VERSION=13.10.9
# Thu, 06 Oct 2022 08:18:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.9
# Thu, 06 Oct 2022 08:18:37 GMT
ENV XWIKI_DOWNLOAD_SHA256=ad57639016b1bfd1cdf84de764b310a65416832645c6bbfd933ec26fd977bb6a
# Thu, 06 Oct 2022 08:19:19 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 06 Oct 2022 08:20:53 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Thu, 06 Oct 2022 08:20:54 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Thu, 06 Oct 2022 08:20:54 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Thu, 06 Oct 2022 08:20:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Thu, 06 Oct 2022 08:20:56 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Thu, 06 Oct 2022 08:20:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 06 Oct 2022 08:20:59 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 06 Oct 2022 08:21:00 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 06 Oct 2022 08:21:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 06 Oct 2022 08:21:02 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 06 Oct 2022 08:21:02 GMT
VOLUME [/usr/local/xwiki]
# Thu, 06 Oct 2022 08:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 08:21:04 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02ffb58034794e0992216f802a3c5320c4b6b9cc80080bdd07eb7afa7db54bd`  
		Last Modified: Wed, 05 Oct 2022 15:52:13 GMT  
		Size: 12.4 MB (12397643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43382a3a0a564d75227f823ea20a3578b988363d9b096c1ac1c03114e9a90ea2`  
		Last Modified: Wed, 05 Oct 2022 15:54:38 GMT  
		Size: 44.8 MB (44824352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de3b9e20aee6838f6495f86ab838f266c1a8a643586fa3020e111e3559d283`  
		Last Modified: Wed, 05 Oct 2022 15:54:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a35f750fc20e703152b852090896888ff46a0f8426adf60a0368838db583d9a`  
		Last Modified: Thu, 06 Oct 2022 04:57:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a663ed3ddb114de1468aa23fa830663c758ce67a9983777fd3c402e8b44042e`  
		Last Modified: Thu, 06 Oct 2022 05:05:18 GMT  
		Size: 12.2 MB (12198650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47516caa6fc59275cfc65dff31f120ecf10b28664133ac9dc4d7e51dd18b33f4`  
		Last Modified: Thu, 06 Oct 2022 05:05:17 GMT  
		Size: 214.3 KB (214348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38b9206ad7676448ddf7d50868d97eb970f5badd523cc330c6d48c0c9651240`  
		Last Modified: Thu, 06 Oct 2022 08:23:05 GMT  
		Size: 173.3 MB (173332338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86feba64bf2f513aeac5b9705b2bfe570fd1b5b126e3d75cbef53d4ff65996c9`  
		Last Modified: Thu, 06 Oct 2022 08:27:02 GMT  
		Size: 292.7 MB (292675939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399b06289c0d6cebeba4b3cac8d459e3251953b7cc81dc18361114e067eae33c`  
		Last Modified: Thu, 06 Oct 2022 08:28:22 GMT  
		Size: 543.9 KB (543935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17024fdb65b298251e35747f8a19245020253d05649de406a1126148b45988`  
		Last Modified: Thu, 06 Oct 2022 08:28:22 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71388f370e7282f13ba298e89063e1c60d578d6f0e0dd69943e157b8c21fbb79`  
		Last Modified: Thu, 06 Oct 2022 08:28:22 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a65223064c93c2e1704268d005ec2ef5cd6037ab841b76dbe2147056e148415`  
		Last Modified: Thu, 06 Oct 2022 08:28:22 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2169596c24fd59a6532b22a02dc6107d6a05a1e999acd8acc330d49a33e7354b`  
		Last Modified: Thu, 06 Oct 2022 08:28:22 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
