<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:12`](#xwiki12)
-	[`xwiki:12-mysql-tomcat`](#xwiki12-mysql-tomcat)
-	[`xwiki:12-postgres-tomcat`](#xwiki12-postgres-tomcat)
-	[`xwiki:12.10`](#xwiki1210)
-	[`xwiki:12.10-mysql-tomcat`](#xwiki1210-mysql-tomcat)
-	[`xwiki:12.10-postgres-tomcat`](#xwiki1210-postgres-tomcat)
-	[`xwiki:12.10.9`](#xwiki12109)
-	[`xwiki:12.10.9-mysql-tomcat`](#xwiki12109-mysql-tomcat)
-	[`xwiki:12.10.9-postgres-tomcat`](#xwiki12109-postgres-tomcat)
-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:13.4`](#xwiki134)
-	[`xwiki:13.4-mysql-tomcat`](#xwiki134-mysql-tomcat)
-	[`xwiki:13.4-postgres-tomcat`](#xwiki134-postgres-tomcat)
-	[`xwiki:13.4.3`](#xwiki1343)
-	[`xwiki:13.4.3-mysql-tomcat`](#xwiki1343-mysql-tomcat)
-	[`xwiki:13.4.3-postgres-tomcat`](#xwiki1343-postgres-tomcat)
-	[`xwiki:13.6`](#xwiki136)
-	[`xwiki:13.6-mysql-tomcat`](#xwiki136-mysql-tomcat)
-	[`xwiki:13.6-postgres-tomcat`](#xwiki136-postgres-tomcat)
-	[`xwiki:13.6.0`](#xwiki1360)
-	[`xwiki:13.6.0-mysql-tomcat`](#xwiki1360-mysql-tomcat)
-	[`xwiki:13.6.0-postgres-tomcat`](#xwiki1360-postgres-tomcat)
-	[`xwiki:latest`](#xwikilatest)
-	[`xwiki:lts`](#xwikilts)
-	[`xwiki:lts-mysql`](#xwikilts-mysql)
-	[`xwiki:lts-mysql-tomcat`](#xwikilts-mysql-tomcat)
-	[`xwiki:lts-postgres`](#xwikilts-postgres)
-	[`xwiki:lts-postgres-tomcat`](#xwikilts-postgres-tomcat)
-	[`xwiki:mysql-tomcat`](#xwikimysql-tomcat)
-	[`xwiki:postgres-tomcat`](#xwikipostgres-tomcat)
-	[`xwiki:stable`](#xwikistable)
-	[`xwiki:stable-mysql`](#xwikistable-mysql)
-	[`xwiki:stable-mysql-tomcat`](#xwikistable-mysql-tomcat)
-	[`xwiki:stable-postgres`](#xwikistable-postgres)
-	[`xwiki:stable-postgres-tomcat`](#xwikistable-postgres-tomcat)

## `xwiki:12`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-postgres-tomcat`

```console
$ docker pull xwiki@sha256:433cf9533b889d4bfccda2860530286de35836069e2f2a27560208534fa23b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0f525ecb54f277d6b340f093aa80018af805a996b401c447ccd1bf745227f07e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.6 MB (718572692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528e7419babf63cf6c07119c25fb621e1715e8c7415625324c62f998916b8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:59 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:23:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:23:39 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:23:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:23:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:23:41 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:23:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f910f4cb265673a9f2aaa4a02d0933452edebb7591054e9063ee896f357b060`  
		Last Modified: Fri, 20 Aug 2021 18:25:53 GMT  
		Size: 297.6 MB (297645317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f87b8fd85f14092e7a0554d57900f3c5b4c6a497d19bb78b56f0d0088134b`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89f145d515d06b267ee77d00be945adba424206e1b8667c1078fb69e32cdae`  
		Last Modified: Fri, 20 Aug 2021 18:25:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4978111291aa16e2ae0b9f66d35fb7b02a000016b586852740d4b5e9352c433`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606644743c6d104ff7cb3521039f8869da601d2621846f98f8f929c43c4ca679`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb23e392044f97e65aabaa782256f9a6ceec3e9a8b9c170bc6abd9d4414f37d`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:729f1979e91cf184756e2de07caba398436947aca19751209f2a4f221d815a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709768945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b9df208bd0e6af6a915c1baf3d1986ec1a3eedf9af37c95c9441e8e1b944cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:41:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:41:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:41:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:41:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:41:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:41:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7713eedc392c7166e541bb275feb5bfcf1ffb4a668670966348111b24816ce3`  
		Last Modified: Fri, 20 Aug 2021 18:42:26 GMT  
		Size: 297.6 MB (297645290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccca645deda106e78a0d3c82adf37bc0cf9d4ff629974256c2d01adcaf1f66`  
		Last Modified: Fri, 20 Aug 2021 18:42:04 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501912f94c9a0000bff48dc623c12daaf7d9a18cff725d0a6c4897a50a41c76`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128dba917691d21b69552d69f21451f3970cf07bbf47ddb7fad39bbe15d42da`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45134541943e8dbedda4039e13b225cf4d9b38b7d93b9b3ddeb06ba241592c`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ab2719986a5b41034e4892648147b568be9e41d881b63294be0ef62ce30c04`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:433cf9533b889d4bfccda2860530286de35836069e2f2a27560208534fa23b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0f525ecb54f277d6b340f093aa80018af805a996b401c447ccd1bf745227f07e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.6 MB (718572692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528e7419babf63cf6c07119c25fb621e1715e8c7415625324c62f998916b8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:59 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:23:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:23:39 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:23:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:23:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:23:41 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:23:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f910f4cb265673a9f2aaa4a02d0933452edebb7591054e9063ee896f357b060`  
		Last Modified: Fri, 20 Aug 2021 18:25:53 GMT  
		Size: 297.6 MB (297645317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f87b8fd85f14092e7a0554d57900f3c5b4c6a497d19bb78b56f0d0088134b`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89f145d515d06b267ee77d00be945adba424206e1b8667c1078fb69e32cdae`  
		Last Modified: Fri, 20 Aug 2021 18:25:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4978111291aa16e2ae0b9f66d35fb7b02a000016b586852740d4b5e9352c433`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606644743c6d104ff7cb3521039f8869da601d2621846f98f8f929c43c4ca679`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb23e392044f97e65aabaa782256f9a6ceec3e9a8b9c170bc6abd9d4414f37d`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:729f1979e91cf184756e2de07caba398436947aca19751209f2a4f221d815a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709768945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b9df208bd0e6af6a915c1baf3d1986ec1a3eedf9af37c95c9441e8e1b944cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:41:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:41:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:41:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:41:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:41:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:41:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7713eedc392c7166e541bb275feb5bfcf1ffb4a668670966348111b24816ce3`  
		Last Modified: Fri, 20 Aug 2021 18:42:26 GMT  
		Size: 297.6 MB (297645290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccca645deda106e78a0d3c82adf37bc0cf9d4ff629974256c2d01adcaf1f66`  
		Last Modified: Fri, 20 Aug 2021 18:42:04 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501912f94c9a0000bff48dc623c12daaf7d9a18cff725d0a6c4897a50a41c76`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128dba917691d21b69552d69f21451f3970cf07bbf47ddb7fad39bbe15d42da`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45134541943e8dbedda4039e13b225cf4d9b38b7d93b9b3ddeb06ba241592c`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ab2719986a5b41034e4892648147b568be9e41d881b63294be0ef62ce30c04`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.9`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.9` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.9-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.9-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.9-postgres-tomcat`

```console
$ docker pull xwiki@sha256:433cf9533b889d4bfccda2860530286de35836069e2f2a27560208534fa23b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10.9-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0f525ecb54f277d6b340f093aa80018af805a996b401c447ccd1bf745227f07e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.6 MB (718572692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528e7419babf63cf6c07119c25fb621e1715e8c7415625324c62f998916b8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:59 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:23:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:23:39 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:23:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:23:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:23:41 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:23:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f910f4cb265673a9f2aaa4a02d0933452edebb7591054e9063ee896f357b060`  
		Last Modified: Fri, 20 Aug 2021 18:25:53 GMT  
		Size: 297.6 MB (297645317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f87b8fd85f14092e7a0554d57900f3c5b4c6a497d19bb78b56f0d0088134b`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89f145d515d06b267ee77d00be945adba424206e1b8667c1078fb69e32cdae`  
		Last Modified: Fri, 20 Aug 2021 18:25:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4978111291aa16e2ae0b9f66d35fb7b02a000016b586852740d4b5e9352c433`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606644743c6d104ff7cb3521039f8869da601d2621846f98f8f929c43c4ca679`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb23e392044f97e65aabaa782256f9a6ceec3e9a8b9c170bc6abd9d4414f37d`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10.9-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:729f1979e91cf184756e2de07caba398436947aca19751209f2a4f221d815a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709768945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b9df208bd0e6af6a915c1baf3d1986ec1a3eedf9af37c95c9441e8e1b944cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:41:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:41:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:41:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:41:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:41:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:41:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7713eedc392c7166e541bb275feb5bfcf1ffb4a668670966348111b24816ce3`  
		Last Modified: Fri, 20 Aug 2021 18:42:26 GMT  
		Size: 297.6 MB (297645290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccca645deda106e78a0d3c82adf37bc0cf9d4ff629974256c2d01adcaf1f66`  
		Last Modified: Fri, 20 Aug 2021 18:42:04 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501912f94c9a0000bff48dc623c12daaf7d9a18cff725d0a6c4897a50a41c76`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128dba917691d21b69552d69f21451f3970cf07bbf47ddb7fad39bbe15d42da`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45134541943e8dbedda4039e13b225cf4d9b38b7d93b9b3ddeb06ba241592c`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ab2719986a5b41034e4892648147b568be9e41d881b63294be0ef62ce30c04`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4`

```console
$ docker pull xwiki@sha256:d7514078d8efcd2208520fca6106864a0823bf587fe428bc72c00c88ee3e53a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4` - linux; amd64

```console
$ docker pull xwiki@sha256:1540f3e25da766107713f2f0f0bc4cc54991e0b2d879481f5834a3e2d4ef5da3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725084146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78b0bcda193c204c4cf7f20176f2055c39c0b6f862a1875380c986d583c2edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:06:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:06:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:06:19 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:06:19 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:06:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684f367c45f33ba67c692ae81a6cdb448039123e1fa2cfce7b055b0796b6b9e`  
		Last Modified: Wed, 18 Aug 2021 12:08:19 GMT  
		Size: 303.5 MB (303492957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dd1d90e51303f81a73b46d55c00cdd26f57eba08f788320e4866fb01b4d27d`  
		Last Modified: Wed, 18 Aug 2021 12:08:02 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92027ece3d5024db7cc7963d562f469186cc05b0ee0246efa1b2d38945ff162b`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ff56690bd24f9a9b7f0b76dd964e5ebce6ebbce05d0b474d1b5fe1c6a0a5eb`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.3 KB (2322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba56ff83b679935b994dcd09d8a75b25bfdca8472babe9215edc9352f50cbe4`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58326a9d6d282394e34d87dac47ef442c8e27d575c3be2e5d8fb809661397f50`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d7514078d8efcd2208520fca6106864a0823bf587fe428bc72c00c88ee3e53a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1540f3e25da766107713f2f0f0bc4cc54991e0b2d879481f5834a3e2d4ef5da3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725084146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78b0bcda193c204c4cf7f20176f2055c39c0b6f862a1875380c986d583c2edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:06:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:06:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:06:19 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:06:19 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:06:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684f367c45f33ba67c692ae81a6cdb448039123e1fa2cfce7b055b0796b6b9e`  
		Last Modified: Wed, 18 Aug 2021 12:08:19 GMT  
		Size: 303.5 MB (303492957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dd1d90e51303f81a73b46d55c00cdd26f57eba08f788320e4866fb01b4d27d`  
		Last Modified: Wed, 18 Aug 2021 12:08:02 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92027ece3d5024db7cc7963d562f469186cc05b0ee0246efa1b2d38945ff162b`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ff56690bd24f9a9b7f0b76dd964e5ebce6ebbce05d0b474d1b5fe1c6a0a5eb`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.3 KB (2322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba56ff83b679935b994dcd09d8a75b25bfdca8472babe9215edc9352f50cbe4`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58326a9d6d282394e34d87dac47ef442c8e27d575c3be2e5d8fb809661397f50`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b5ff8a29141128c501d30b937cece2f9470bc822b93740b084273914b4ddb8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b15c40eba84c4840213b75c1d24e3de33abb355d3a5558de12d945fa4eaca2af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.4 MB (724420176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c4df15a8ee61bf42823678b6677af12a157e9a57d17586fda08d4fa96206b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:06:26 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:06:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:06:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:07:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:07:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 18 Aug 2021 12:07:07 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:07:08 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:07:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:07:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:07:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:07:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfbc0c18534775a0a19ea6b0c660c4e56af7e8c56f77286f575520da47e5a`  
		Last Modified: Wed, 18 Aug 2021 12:08:54 GMT  
		Size: 303.5 MB (303492840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3051b298b1b60ddcf9fb4a31de8749eff01e98b7bf57cd89ad6a5f9897e5ae8`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043334b0d68d492dd354de7be16bc79755e99cb101687c59466da8e7f26899b`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854116fb04aab2e59c9a4d6c9b3e360daa5db9e80c89cb9f6e75883078f7c2b1`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781e338907f158c486e046aed977e58916d87bf6c9afb61fecb291ce96f92dac`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d64de4129d2a253cbefa24b78f0db64b95a950f3444d43192b8743a29f025`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:987e0d7651b6cb61b6dd18391993b6afa124568de88bb707ecdb6e7313841567
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715616446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65410d6a68e68b605a278841294da759e91d3372f4a924a2ff33d4612d133321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 07:59:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 07:59:14 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 18 Aug 2021 07:59:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 07:59:14 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 07:59:15 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 07:59:15 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 07:59:15 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 07:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 07:59:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924b4ab462b87594f47f5efb9b6addce510c8ac3052ba07d793fe245bba85d4`  
		Last Modified: Wed, 18 Aug 2021 08:00:28 GMT  
		Size: 303.5 MB (303492854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c718d1e9e5874187fb15ca358143d1679dedca95fd967d63cfdf9897e48eb`  
		Last Modified: Wed, 18 Aug 2021 08:00:05 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b521aa21f2abccbbf08616fdb7215f41a15345556b70b746b9c496cd6d537ec3`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238492517eb9d8875f20680d7e216f32e3f734aaed2d7d4663fd91e6d95df8a8`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705270bee10d491549344b23b93baa964193df9ce0bd28dfc17e564fea2c4127`  
		Last Modified: Wed, 18 Aug 2021 08:00:05 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11fdcda348dd7c9af9cbebba5ee1171801edf1219b8641e9ed5cc06fdf09b90`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3`

```console
$ docker pull xwiki@sha256:d7514078d8efcd2208520fca6106864a0823bf587fe428bc72c00c88ee3e53a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.3` - linux; amd64

```console
$ docker pull xwiki@sha256:1540f3e25da766107713f2f0f0bc4cc54991e0b2d879481f5834a3e2d4ef5da3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725084146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78b0bcda193c204c4cf7f20176f2055c39c0b6f862a1875380c986d583c2edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:06:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:06:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:06:19 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:06:19 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:06:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684f367c45f33ba67c692ae81a6cdb448039123e1fa2cfce7b055b0796b6b9e`  
		Last Modified: Wed, 18 Aug 2021 12:08:19 GMT  
		Size: 303.5 MB (303492957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dd1d90e51303f81a73b46d55c00cdd26f57eba08f788320e4866fb01b4d27d`  
		Last Modified: Wed, 18 Aug 2021 12:08:02 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92027ece3d5024db7cc7963d562f469186cc05b0ee0246efa1b2d38945ff162b`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ff56690bd24f9a9b7f0b76dd964e5ebce6ebbce05d0b474d1b5fe1c6a0a5eb`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.3 KB (2322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba56ff83b679935b994dcd09d8a75b25bfdca8472babe9215edc9352f50cbe4`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58326a9d6d282394e34d87dac47ef442c8e27d575c3be2e5d8fb809661397f50`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d7514078d8efcd2208520fca6106864a0823bf587fe428bc72c00c88ee3e53a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.3-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1540f3e25da766107713f2f0f0bc4cc54991e0b2d879481f5834a3e2d4ef5da3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725084146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78b0bcda193c204c4cf7f20176f2055c39c0b6f862a1875380c986d583c2edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:05:36 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:06:15 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Wed, 18 Aug 2021 12:06:16 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:17 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Wed, 18 Aug 2021 12:06:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:06:18 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:06:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:06:19 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:06:19 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:06:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684f367c45f33ba67c692ae81a6cdb448039123e1fa2cfce7b055b0796b6b9e`  
		Last Modified: Wed, 18 Aug 2021 12:08:19 GMT  
		Size: 303.5 MB (303492957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dd1d90e51303f81a73b46d55c00cdd26f57eba08f788320e4866fb01b4d27d`  
		Last Modified: Wed, 18 Aug 2021 12:08:02 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92027ece3d5024db7cc7963d562f469186cc05b0ee0246efa1b2d38945ff162b`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ff56690bd24f9a9b7f0b76dd964e5ebce6ebbce05d0b474d1b5fe1c6a0a5eb`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.3 KB (2322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba56ff83b679935b994dcd09d8a75b25bfdca8472babe9215edc9352f50cbe4`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58326a9d6d282394e34d87dac47ef442c8e27d575c3be2e5d8fb809661397f50`  
		Last Modified: Wed, 18 Aug 2021 12:08:01 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3-postgres-tomcat`

```console
$ docker pull xwiki@sha256:b5ff8a29141128c501d30b937cece2f9470bc822b93740b084273914b4ddb8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4.3-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:b15c40eba84c4840213b75c1d24e3de33abb355d3a5558de12d945fa4eaca2af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.4 MB (724420176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c4df15a8ee61bf42823678b6677af12a157e9a57d17586fda08d4fa96206b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 12:06:26 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 12:06:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 12:06:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 12:07:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 12:07:07 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 18 Aug 2021 12:07:07 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 12:07:08 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 12:07:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 12:07:09 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 12:07:09 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 12:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 12:07:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfbc0c18534775a0a19ea6b0c660c4e56af7e8c56f77286f575520da47e5a`  
		Last Modified: Wed, 18 Aug 2021 12:08:54 GMT  
		Size: 303.5 MB (303492840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3051b298b1b60ddcf9fb4a31de8749eff01e98b7bf57cd89ad6a5f9897e5ae8`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043334b0d68d492dd354de7be16bc79755e99cb101687c59466da8e7f26899b`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854116fb04aab2e59c9a4d6c9b3e360daa5db9e80c89cb9f6e75883078f7c2b1`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781e338907f158c486e046aed977e58916d87bf6c9afb61fecb291ce96f92dac`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d64de4129d2a253cbefa24b78f0db64b95a950f3444d43192b8743a29f025`  
		Last Modified: Wed, 18 Aug 2021 12:08:36 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4.3-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:987e0d7651b6cb61b6dd18391993b6afa124568de88bb707ecdb6e7313841567
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.6 MB (715616446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65410d6a68e68b605a278841294da759e91d3372f4a924a2ff33d4612d133321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_VERSION=13.4.3
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Wed, 18 Aug 2021 07:58:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Wed, 18 Aug 2021 07:59:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 18 Aug 2021 07:59:14 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 18 Aug 2021 07:59:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 18 Aug 2021 07:59:14 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 18 Aug 2021 07:59:15 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 18 Aug 2021 07:59:15 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 18 Aug 2021 07:59:15 GMT
VOLUME [/usr/local/xwiki]
# Wed, 18 Aug 2021 07:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Aug 2021 07:59:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924b4ab462b87594f47f5efb9b6addce510c8ac3052ba07d793fe245bba85d4`  
		Last Modified: Wed, 18 Aug 2021 08:00:28 GMT  
		Size: 303.5 MB (303492854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c718d1e9e5874187fb15ca358143d1679dedca95fd967d63cfdf9897e48eb`  
		Last Modified: Wed, 18 Aug 2021 08:00:05 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b521aa21f2abccbbf08616fdb7215f41a15345556b70b746b9c496cd6d537ec3`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238492517eb9d8875f20680d7e216f32e3f734aaed2d7d4663fd91e6d95df8a8`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705270bee10d491549344b23b93baa964193df9ce0bd28dfc17e564fea2c4127`  
		Last Modified: Wed, 18 Aug 2021 08:00:05 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11fdcda348dd7c9af9cbebba5ee1171801edf1219b8641e9ed5cc06fdf09b90`  
		Last Modified: Wed, 18 Aug 2021 08:00:04 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.6` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6-mysql-tomcat`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.6-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6-postgres-tomcat`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.6-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.6-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6.0`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.6.0` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.6.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.6.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.6.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.6.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:d2ef583cc4258411ac1c983b6b8832ef2d9b297cfdcd6c6d2a51ab1c097708bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:448fe21170c7f1ee249c32b7446559e7292cb4eccf7ba71171089dcc558d21b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.2 MB (719236553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081f32ee95c15d0c15171f2174dee801326b3d7e04adb54b68f7fcc7ca646a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:22:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:22:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:22:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:50 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 20 Aug 2021 18:22:51 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 20 Aug 2021 18:22:51 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:22:52 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:22:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:22:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:22:53 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:22:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6e1a392e341f73bd7f7400713ee3c92f7150763999c31b53e6adf79a8c27b`  
		Last Modified: Fri, 20 Aug 2021 18:24:55 GMT  
		Size: 297.6 MB (297645314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3226e653aff3320ea63b325f7dcfeea6bc465ce4d86e588e545b919899600`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 MB (2257820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c4b47e5d8b4ee6dc7c32a0714636cce32b4931d7789fe519247fcd8278d3f8`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc67010117843b97028010bb1b4d329f1a76ef8f7c36c5c7de64a746a2210615`  
		Last Modified: Fri, 20 Aug 2021 18:24:37 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c9f226f4ba54bf0d9766652f4619d027246dbcda0849cc698e18742a93fdc`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4319deb42214bd2b53dfce04d44215b11fe15089ff9a187b099ba8add8cca2d5`  
		Last Modified: Fri, 20 Aug 2021 18:24:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:433cf9533b889d4bfccda2860530286de35836069e2f2a27560208534fa23b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:0f525ecb54f277d6b340f093aa80018af805a996b401c447ccd1bf745227f07e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.6 MB (718572692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528e7419babf63cf6c07119c25fb621e1715e8c7415625324c62f998916b8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:59 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:23:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:23:39 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:23:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:23:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:23:41 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:23:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f910f4cb265673a9f2aaa4a02d0933452edebb7591054e9063ee896f357b060`  
		Last Modified: Fri, 20 Aug 2021 18:25:53 GMT  
		Size: 297.6 MB (297645317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f87b8fd85f14092e7a0554d57900f3c5b4c6a497d19bb78b56f0d0088134b`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89f145d515d06b267ee77d00be945adba424206e1b8667c1078fb69e32cdae`  
		Last Modified: Fri, 20 Aug 2021 18:25:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4978111291aa16e2ae0b9f66d35fb7b02a000016b586852740d4b5e9352c433`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606644743c6d104ff7cb3521039f8869da601d2621846f98f8f929c43c4ca679`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb23e392044f97e65aabaa782256f9a6ceec3e9a8b9c170bc6abd9d4414f37d`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:729f1979e91cf184756e2de07caba398436947aca19751209f2a4f221d815a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709768945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b9df208bd0e6af6a915c1baf3d1986ec1a3eedf9af37c95c9441e8e1b944cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:41:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:41:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:41:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:41:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:41:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:41:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7713eedc392c7166e541bb275feb5bfcf1ffb4a668670966348111b24816ce3`  
		Last Modified: Fri, 20 Aug 2021 18:42:26 GMT  
		Size: 297.6 MB (297645290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccca645deda106e78a0d3c82adf37bc0cf9d4ff629974256c2d01adcaf1f66`  
		Last Modified: Fri, 20 Aug 2021 18:42:04 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501912f94c9a0000bff48dc623c12daaf7d9a18cff725d0a6c4897a50a41c76`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128dba917691d21b69552d69f21451f3970cf07bbf47ddb7fad39bbe15d42da`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45134541943e8dbedda4039e13b225cf4d9b38b7d93b9b3ddeb06ba241592c`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ab2719986a5b41034e4892648147b568be9e41d881b63294be0ef62ce30c04`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:433cf9533b889d4bfccda2860530286de35836069e2f2a27560208534fa23b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0f525ecb54f277d6b340f093aa80018af805a996b401c447ccd1bf745227f07e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.6 MB (718572692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528e7419babf63cf6c07119c25fb621e1715e8c7415625324c62f998916b8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:22:59 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:23:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:23:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:23:39 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:23:40 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:23:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:23:41 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:23:41 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:23:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f910f4cb265673a9f2aaa4a02d0933452edebb7591054e9063ee896f357b060`  
		Last Modified: Fri, 20 Aug 2021 18:25:53 GMT  
		Size: 297.6 MB (297645317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f87b8fd85f14092e7a0554d57900f3c5b4c6a497d19bb78b56f0d0088134b`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89f145d515d06b267ee77d00be945adba424206e1b8667c1078fb69e32cdae`  
		Last Modified: Fri, 20 Aug 2021 18:25:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4978111291aa16e2ae0b9f66d35fb7b02a000016b586852740d4b5e9352c433`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606644743c6d104ff7cb3521039f8869da601d2621846f98f8f929c43c4ca679`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb23e392044f97e65aabaa782256f9a6ceec3e9a8b9c170bc6abd9d4414f37d`  
		Last Modified: Fri, 20 Aug 2021 18:25:35 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:729f1979e91cf184756e2de07caba398436947aca19751209f2a4f221d815a6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709768945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b9df208bd0e6af6a915c1baf3d1986ec1a3eedf9af37c95c9441e8e1b944cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_VERSION=12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.9
# Fri, 20 Aug 2021 18:40:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=3620d66821e9729e43aa8f801e89184ab9d29feefb634eeb155b28bb9452df4d
# Fri, 20 Aug 2021 18:41:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 20 Aug 2021 18:41:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 20 Aug 2021 18:41:13 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 20 Aug 2021 18:41:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 20 Aug 2021 18:41:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 20 Aug 2021 18:41:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Aug 2021 18:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Aug 2021 18:41:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7713eedc392c7166e541bb275feb5bfcf1ffb4a668670966348111b24816ce3`  
		Last Modified: Fri, 20 Aug 2021 18:42:26 GMT  
		Size: 297.6 MB (297645290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccca645deda106e78a0d3c82adf37bc0cf9d4ff629974256c2d01adcaf1f66`  
		Last Modified: Fri, 20 Aug 2021 18:42:04 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501912f94c9a0000bff48dc623c12daaf7d9a18cff725d0a6c4897a50a41c76`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128dba917691d21b69552d69f21451f3970cf07bbf47ddb7fad39bbe15d42da`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45134541943e8dbedda4039e13b225cf4d9b38b7d93b9b3ddeb06ba241592c`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ab2719986a5b41034e4892648147b568be9e41d881b63294be0ef62ce30c04`  
		Last Modified: Fri, 20 Aug 2021 18:42:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:e665b34029c5ae78d970fba38f2579bffe5927574dbf4e4d293ced89dc58daac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cf483ec0d4b04883925ec50778da7474d5d5385de70918dd6a773158fa01c11a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726092725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67f1b8bbb2c92d44f3d2b37dbfe49a7ed5e33e06e855cea598f36afbbad0bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:02:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:02:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:02:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:03:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:03:29 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:30 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Tue, 17 Aug 2021 01:03:31 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:03:31 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:03:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:03:32 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:03:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:03:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63cd20b23c6c1590889695f4c89e488c32305de0221e1e9594d8bd80c94d6b0`  
		Last Modified: Tue, 17 Aug 2021 01:09:35 GMT  
		Size: 167.5 MB (167473419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bf7c52656747389a88f926271f47b040eee575c98c56fa21845fcee1f0481`  
		Last Modified: Tue, 17 Aug 2021 01:09:29 GMT  
		Size: 304.5 MB (304501533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24381f11bbc7d66e54032bcaea976ba37d05a7cfba2ff4b21ea8ac72ff9e2c`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 MB (2257824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ace60118d65d089df109e4656235f3f0502d894758dc83bdd16dcdcb796e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ef466f54b1b441844e4f96ef56e1b6cc134ef35e17b549815272c2c05e86e8`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.3 KB (2321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fefb75f2891ee6808782dbc534d3757909689aa7c047a1925a5dd303495b8db`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9652414cf2087990a49304b2f206a986f821a1b68cb14fe39f85df0e379ef`  
		Last Modified: Tue, 17 Aug 2021 01:09:09 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:020deec841654c9a10992fec6b30837f350bc4f33c70408c0f97548afd20582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8b1a7ff69f12422a587995e31744ec59788e89cfe9c0f08acfa9541ee24a0eda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.4 MB (725428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7404bcd47689e7e955059c1b3e73b25813457c9ccfbceda237e9703cae19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:59:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:18 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 23:00:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 23:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 23:00:28 GMT
CMD ["jshell"]
# Wed, 28 Jul 2021 23:59:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 28 Jul 2021 23:59:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jul 2021 23:59:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 28 Jul 2021 23:59:17 GMT
WORKDIR /usr/local/tomcat
# Wed, 28 Jul 2021 23:59:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 28 Jul 2021 23:59:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:09:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:09:33 GMT
ENV TOMCAT_MAJOR=8
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_VERSION=8.5.70
# Tue, 17 Aug 2021 00:26:10 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Tue, 17 Aug 2021 00:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 17 Aug 2021 00:27:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 17 Aug 2021 00:27:23 GMT
EXPOSE 8080
# Tue, 17 Aug 2021 00:27:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 01:00:50 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 01:04:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 01:04:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 01:04:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 01:04:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 01:04:57 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 01:04:57 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 01:04:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 01:04:58 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 01:04:58 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 01:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 01:04:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63509f5b973d2357463075b878f6ff9177d80ba67e8544cc72eaf22ae30959`  
		Last Modified: Mon, 26 Jul 2021 23:09:43 GMT  
		Size: 16.0 MB (16033263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d7b43f221b36cd41283789af5d5c79d64a5a47c627fa8295a0f307a00aa861`  
		Last Modified: Mon, 26 Jul 2021 23:10:34 GMT  
		Size: 193.7 MB (193651025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a9bd959def86cb1074d29ddfa68f6bd98357e5ee11952298483e89edede0d`  
		Last Modified: Thu, 29 Jul 2021 00:16:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8047822be9e479c27bf15e0b5c9a62756ca46d323571f6aa9a7d5255780a61`  
		Last Modified: Tue, 17 Aug 2021 00:39:39 GMT  
		Size: 13.6 MB (13596057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd187c5d5a6acf81a742878194eac3c83e81faf4941c6d822bf9de088443831b`  
		Last Modified: Tue, 17 Aug 2021 00:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1026ae2d54441ff0349f8a81037a46ba697cc93b28e96a9d5e0177eca45084`  
		Last Modified: Tue, 17 Aug 2021 01:10:42 GMT  
		Size: 168.3 MB (168271819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b8bf6c5edff446d560be9d4902db26b287a23d8a8389c5ebdcc73975511a6`  
		Last Modified: Tue, 17 Aug 2021 01:10:36 GMT  
		Size: 304.5 MB (304501546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f732b79624c7f1d91aa8a5b64e95e52364a20b322424318576bcbd07ebb1f3`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 795.4 KB (795417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b21526b3c5bf34096c4ae1369de4346145f81dc605640780f474578985d5ec`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7bfcbbc49ae4c61832cd63d8395ff3522f5609f3284513e2c87dc092b6027`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7900adb2e41820bdac0f334ea50e32fdc5f2414aaa2ee4f275a0f444e84accd`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f50e8ac47271d93cac9edf269ec9547eead42993ec094ec1706f502ad1bedc`  
		Last Modified: Tue, 17 Aug 2021 01:10:15 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a9bcdb7c48fa3fce98813bfcfc293ef3553a7e6f697fbf622299f5fe9b6018bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716625086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83224fe6ca74d036b5b6081b4187aa21595fa333411e4353551b6f0ee52cfcb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jul 2021 22:15:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 26 Jul 2021 22:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 26 Jul 2021 22:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 22:15:52 GMT
CMD ["jshell"]
# Thu, 29 Jul 2021 00:27:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Jul 2021 00:27:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jul 2021 00:27:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Jul 2021 00:27:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Jul 2021 00:27:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:27:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Jul 2021 00:40:28 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 29 Jul 2021 00:40:28 GMT
ENV TOMCAT_MAJOR=8
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 16 Aug 2021 23:48:55 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 16 Aug 2021 23:49:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 16 Aug 2021 23:49:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 16 Aug 2021 23:49:39 GMT
EXPOSE 8080
# Mon, 16 Aug 2021 23:49:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 17 Aug 2021 00:27:37 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 17 Aug 2021 00:28:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_VERSION=13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.6
# Tue, 17 Aug 2021 00:28:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=58518900cd01cc8445e0fb098c33d721070180f26542fdce9ce38677c0b06dab
# Tue, 17 Aug 2021 00:28:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 17 Aug 2021 00:28:50 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 17 Aug 2021 00:28:50 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 17 Aug 2021 00:28:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 17 Aug 2021 00:28:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Aug 2021 00:28:51 GMT
VOLUME [/usr/local/xwiki]
# Tue, 17 Aug 2021 00:28:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 00:28:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcc4ceb51ac08370be105d7f328e8fe57475e20b0b894a485dbdbfa93e0fbc`  
		Last Modified: Mon, 26 Jul 2021 22:18:58 GMT  
		Size: 15.9 MB (15894651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d2605e876547e87f844503ba2e3c9671f2c311e6a5f68aa2f81793abdfad3a`  
		Last Modified: Mon, 26 Jul 2021 22:20:01 GMT  
		Size: 190.4 MB (190379257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7bfff8136926f55f341d27d27e5756ffdeab81f13137877af6d47881ac1e83`  
		Last Modified: Thu, 29 Jul 2021 00:50:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd080521844520d640c7a534ee2fd4977b26666e743cef291f7b532e990682f`  
		Last Modified: Tue, 17 Aug 2021 00:05:17 GMT  
		Size: 13.5 MB (13485468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243acc44db9b022adf93321fb01da337d5ecdd875375ec9985a48aa7f484bbbe`  
		Last Modified: Tue, 17 Aug 2021 00:05:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33c07878957321b74dfc1cb1192759de4214c8bed0c3bfef884e78153d7eeb3`  
		Last Modified: Tue, 17 Aug 2021 00:31:50 GMT  
		Size: 164.4 MB (164386747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffa0a214636c23d04fcc8cc1840e23436fe205695b90062c0247d4b1fb3eaa`  
		Last Modified: Tue, 17 Aug 2021 00:31:42 GMT  
		Size: 304.5 MB (304501492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505006a75d81a04154d2aedfef5b85db39c95c28dd9b8ce379c4e81545dfeb5`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8cfd9d5c32263eb24c0ce74797a43a1b4217d61361f49b172a34f5a1d82205`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cc5f635f96cef5f0d5dc599a3ee19f8de342de5e8a21a2c10eb018a847a69`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f51f8eb6c12b7d98fa301a1cd4152e39cb5d096d069f16b049fb8d4db783429`  
		Last Modified: Tue, 17 Aug 2021 00:31:18 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cd9962afe257781479445d4d052a9f4def6130b6647d07ab108a1377216edf`  
		Last Modified: Tue, 17 Aug 2021 00:31:19 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
