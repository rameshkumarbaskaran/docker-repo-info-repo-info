## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:5b4eb951c935d675877242440ad972ee19aa149d87329e460a34fc4310dfdd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0b4cec8521d6fdb79fd7d48fc56afa77ab54656507b61fee9d488268ec505d80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 MB (631015401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2e08968d9483d4946cba161453cee29d3547ea6d9e676b5ce08bcc31256eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:53:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 02 Aug 2022 05:53:35 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 02 Aug 2022 05:53:35 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 05:53:35 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:53:35 GMT
ENV JAVA_VERSION=11.0.16
# Tue, 02 Aug 2022 05:53:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 03 Aug 2022 04:50:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 04:50:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:50:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 04:50:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 04:50:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 04:50:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 05:00:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 03 Aug 2022 05:00:40 GMT
ENV TOMCAT_MAJOR=9
# Wed, 03 Aug 2022 05:00:40 GMT
ENV TOMCAT_VERSION=9.0.65
# Wed, 03 Aug 2022 05:00:40 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Wed, 03 Aug 2022 05:00:41 GMT
COPY dir:65dd5ac50766599795e77577cb99e06ab5d40467f701cdbf7b34e61fc84ea5d5 in /usr/local/tomcat 
# Wed, 03 Aug 2022 05:00:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:00:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 05:00:45 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:00:46 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Aug 2022 14:55:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Aug 2022 14:56:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 15:00:27 GMT
ENV XWIKI_VERSION=13.10.8
# Wed, 03 Aug 2022 15:00:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.8
# Wed, 03 Aug 2022 15:00:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=d6da0bdfb5e0c9e5acccd13a9ff2d40a5bda2a3f9db4426f58fe8f47c262f4b7
# Wed, 03 Aug 2022 15:01:05 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 03 Aug 2022 15:01:07 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Wed, 03 Aug 2022 15:01:07 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Wed, 03 Aug 2022 15:01:07 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Wed, 03 Aug 2022 15:01:07 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Wed, 03 Aug 2022 15:01:07 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Wed, 03 Aug 2022 15:01:08 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 03 Aug 2022 15:01:08 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 03 Aug 2022 15:01:08 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 03 Aug 2022 15:01:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 03 Aug 2022 15:01:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 03 Aug 2022 15:01:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Aug 2022 15:01:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 15:01:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8510da692cda60e4746c14dd90905695eade5888e2ad640706a2be9dc42a0224`  
		Last Modified: Tue, 02 Aug 2022 06:11:48 GMT  
		Size: 5.7 MB (5657904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d84395b34d8ae99a6c83b1da729fdfc0678767272973ada75ed7772572e392`  
		Last Modified: Tue, 02 Aug 2022 06:11:47 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03fea6c3ad764587adf11c70121a7bb47883183ea13fb6b9f73727caf2a6f7`  
		Last Modified: Tue, 02 Aug 2022 06:11:54 GMT  
		Size: 45.8 MB (45770339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16035ba6c4fdbdfa49325cd520facbf7a831d79dd2a054746fb334e9d4c23293`  
		Last Modified: Wed, 03 Aug 2022 05:34:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a325c9880603ccf5f8820e80fcd776ebd9b3a9270ceb83585b0fb3132cb07`  
		Last Modified: Wed, 03 Aug 2022 05:45:00 GMT  
		Size: 12.2 MB (12160190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47caff8ca9e18332210def7df3e32db9360973deaa77abd21ea6952010250075`  
		Last Modified: Wed, 03 Aug 2022 05:44:59 GMT  
		Size: 459.7 KB (459720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daf3316826880ad73a537db6d69aeb694497811d7769923112d92b452ca007`  
		Last Modified: Wed, 03 Aug 2022 05:44:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82a60eeabecfe17ee5bb89642b80210f888dd51db0469dd4d36c8b40ad98e73`  
		Last Modified: Wed, 03 Aug 2022 15:03:28 GMT  
		Size: 200.9 MB (200883439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5783350f350b5bf9155529a26d514562d981991c1a816c275dab43b6a19b1f7`  
		Last Modified: Wed, 03 Aug 2022 15:07:44 GMT  
		Size: 292.7 MB (292658587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a4d918b8ac62edcbbb09f8d4e667ddc0b6d155937654a4a402845d64e46110`  
		Last Modified: Wed, 03 Aug 2022 15:07:27 GMT  
		Size: 2.4 MB (2381170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaab024ac3604aa86bca15879274d9fbeb2a3b3cc30088d4c958bd0599c8a20`  
		Last Modified: Wed, 03 Aug 2022 15:07:27 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebaf15e11f73aaf30dee0c245e14b4af4c8a51e6de0940e3d3922ccdb982b9d`  
		Last Modified: Wed, 03 Aug 2022 15:07:27 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8729584f270e96481264240c4f5a7006bd2f0e49d28fc0c416af6612028e25f1`  
		Last Modified: Wed, 03 Aug 2022 15:07:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503de81325c8666483d06dd3c8a63e072978ce657e7f52884dd783f39ca210fc`  
		Last Modified: Wed, 03 Aug 2022 15:07:27 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:edbbbb678b50e4e617c5fa466edcb516384e9b90162ccee2acbf67f312ba9e3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.4 MB (566420859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153b6cdd826254cbc1694eff5727c86835c485d30b1eb2e4a313478fccbab29b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:40:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:40:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 19:41:05 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:41:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Aug 2022 19:41:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 21:20:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Aug 2022 21:20:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 21:20:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Aug 2022 21:20:23 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Aug 2022 21:20:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Aug 2022 21:20:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Aug 2022 21:30:16 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Aug 2022 21:30:17 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Aug 2022 21:30:18 GMT
ENV TOMCAT_VERSION=9.0.65
# Wed, 24 Aug 2022 21:30:19 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Wed, 24 Aug 2022 21:30:21 GMT
COPY dir:61f3b0b84c95fbd33c379e9173b35a8724f3ac23ab9c8da0525ca9cedeef1145 in /usr/local/tomcat 
# Wed, 24 Aug 2022 21:30:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 21:30:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Aug 2022 21:30:30 GMT
EXPOSE 8080
# Wed, 24 Aug 2022 21:30:31 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Aug 2022 19:03:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Aug 2022 19:03:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Aug 2022 19:03:07 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Aug 2022 19:03:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Aug 2022 19:03:09 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Aug 2022 19:03:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Aug 2022 19:03:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Mon, 29 Aug 2022 19:09:13 GMT
ENV XWIKI_VERSION=13.10.8
# Mon, 29 Aug 2022 19:09:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.8
# Mon, 29 Aug 2022 19:09:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=d6da0bdfb5e0c9e5acccd13a9ff2d40a5bda2a3f9db4426f58fe8f47c262f4b7
# Mon, 29 Aug 2022 19:09:57 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 29 Aug 2022 19:09:58 GMT
ENV MYSQL_JDBC_VERSION=8.0.30
# Mon, 29 Aug 2022 19:09:59 GMT
ENV MYSQL_JDBC_SHA256=b5bf2f0987197c30adf74a9e419b89cda4c257da2d1142871f508416d5f2227a
# Mon, 29 Aug 2022 19:10:00 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.30
# Mon, 29 Aug 2022 19:10:01 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.30.jar
# Mon, 29 Aug 2022 19:10:02 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.30.jar
# Mon, 29 Aug 2022 19:10:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Mon, 29 Aug 2022 19:10:05 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 29 Aug 2022 19:10:06 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 29 Aug 2022 19:10:07 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 29 Aug 2022 19:10:08 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 29 Aug 2022 19:10:08 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Aug 2022 19:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Aug 2022 19:10:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a729bc90f861d8ccd964a45b6f12093afcb2172c43390409a73e938d36aa1a`  
		Last Modified: Fri, 12 Aug 2022 17:51:29 GMT  
		Size: 12.4 MB (12414351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042d81bb6b9272594d41df4317c8cf379d5be12ec7996d43c3ff4895df8f7481`  
		Last Modified: Wed, 24 Aug 2022 19:48:46 GMT  
		Size: 44.8 MB (44826689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43604d6aa5b7375e91eff36fad8ec1318a6778b92030981be3df7a05dd83427`  
		Last Modified: Wed, 24 Aug 2022 19:48:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f4ffb2ea5560a3bd73f2a4330ac7bb7ac6fa090a621775164836bad8d7b6b7`  
		Last Modified: Wed, 24 Aug 2022 21:49:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a769d4756b889f1731b5a45381c4c8201ef34c9f17d41190afc013b549bf4dc4`  
		Last Modified: Wed, 24 Aug 2022 21:58:03 GMT  
		Size: 12.2 MB (12191517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf5121ba4d99957a68a6f13ebfc857a9d43d83e93ec97e7d5468195af81e6d8`  
		Last Modified: Wed, 24 Aug 2022 21:58:01 GMT  
		Size: 214.4 KB (214396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0de79d874a72e9cc6f0da5d66326955c607dac2cbfb69f31074dc9e5936a5`  
		Last Modified: Mon, 29 Aug 2022 19:13:40 GMT  
		Size: 173.3 MB (173346883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e031b11ad65b445acf5f27fdc2781009c021fe98c9b2281c98e2c3a460030a`  
		Last Modified: Mon, 29 Aug 2022 19:17:56 GMT  
		Size: 292.7 MB (292658839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cad8de79383809b3c09ab06aabdd722af591a1ba570ffe05ff6d6e27765f3d`  
		Last Modified: Mon, 29 Aug 2022 19:17:35 GMT  
		Size: 2.4 MB (2375237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f814988fb1bcbbbe8684f24c97b2a1448740a134bd5008da1f3a7b1f16ee3f6`  
		Last Modified: Mon, 29 Aug 2022 19:17:34 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213190e34c4ae5eebd0585475b55dda04e22226be184704dd73a17e0fc492ed`  
		Last Modified: Mon, 29 Aug 2022 19:17:34 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf3186f48c0cf5dd5befe11608216e0574ccb638af83c7ee466c476a3104e4a`  
		Last Modified: Mon, 29 Aug 2022 19:17:34 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aad2073285a681d29383ca990d954e70f07c515060d8cf7161f563145d851`  
		Last Modified: Mon, 29 Aug 2022 19:17:34 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
