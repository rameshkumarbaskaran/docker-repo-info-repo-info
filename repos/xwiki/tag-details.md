<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:12`](#xwiki12)
-	[`xwiki:12-mysql-tomcat`](#xwiki12-mysql-tomcat)
-	[`xwiki:12-postgres-tomcat`](#xwiki12-postgres-tomcat)
-	[`xwiki:12.10`](#xwiki1210)
-	[`xwiki:12.10-mysql-tomcat`](#xwiki1210-mysql-tomcat)
-	[`xwiki:12.10-postgres-tomcat`](#xwiki1210-postgres-tomcat)
-	[`xwiki:12.10.10`](#xwiki121010)
-	[`xwiki:12.10.10-mysql-tomcat`](#xwiki121010-mysql-tomcat)
-	[`xwiki:12.10.10-postgres-tomcat`](#xwiki121010-postgres-tomcat)
-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:13.4`](#xwiki134)
-	[`xwiki:13.4-mysql-tomcat`](#xwiki134-mysql-tomcat)
-	[`xwiki:13.4-postgres-tomcat`](#xwiki134-postgres-tomcat)
-	[`xwiki:13.4.3`](#xwiki1343)
-	[`xwiki:13.4.3-mysql-tomcat`](#xwiki1343-mysql-tomcat)
-	[`xwiki:13.4.3-postgres-tomcat`](#xwiki1343-postgres-tomcat)
-	[`xwiki:13.8`](#xwiki138)
-	[`xwiki:13.8-mysql-tomcat`](#xwiki138-mysql-tomcat)
-	[`xwiki:13.8-postgres-tomcat`](#xwiki138-postgres-tomcat)
-	[`xwiki:13.8.0`](#xwiki1380)
-	[`xwiki:13.8.0-mysql-tomcat`](#xwiki1380-mysql-tomcat)
-	[`xwiki:13.8.0-postgres-tomcat`](#xwiki1380-postgres-tomcat)
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
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-mysql-tomcat`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-postgres-tomcat`

```console
$ docker pull xwiki@sha256:67bd3a30bd978a0c6c785753a32fa3959287216bc1fab41d7b976889c89b8ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22264a0e41f5d1bdb578aef073fc0be9e98b87b520c237233e320e219087da73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.9 MB (716866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa444e12f457ad05650c24cf66fd1407d7066e670c6bf9af0280ab54e63f0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:21:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:21:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 08 Oct 2021 23:21:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:21:46 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:21:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:21:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:21:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:21:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ec7855604de4410f6b633da69fc863f74332acab6411ac7726decc4591421`  
		Last Modified: Fri, 08 Oct 2021 23:23:42 GMT  
		Size: 297.7 MB (297665999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b36beadc0e3f9eb2ab9b771d8c50c067a63c85122fa0e247d9b059d211ca01`  
		Last Modified: Fri, 08 Oct 2021 23:23:25 GMT  
		Size: 795.4 KB (795419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04803a6e88ed7004bbdad416bec1782e9fd14dc80753767f0b3943e01123bbfb`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45696640937fd910d83c0057455bab285b7ddd3747fd5f58789999219807f1`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acac556405b1d66473149a0aeeb6d67ce5cdceed14d288b1cb15728441dcc9be`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e5ada93951ebc56fde42c610817441b784bb8184288f296f99a55a68ca3a4`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b5343ba912f4ac7359356079c433b6bfdf9d69895a2fb586e8d115e595714824
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.7 MB (707674973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2aa3a4b8e73028c6b94db8a38da1d5be5691ad5ed17a4106a228bd68f8e401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:14:14 GMT
ENV XWIKI_VERSION=12.10.10
# Thu, 14 Oct 2021 03:14:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Thu, 14 Oct 2021 03:14:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Thu, 14 Oct 2021 03:15:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:15:27 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:15:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:15:29 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:15:30 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:15:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:15:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:15:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c372ded7cdd263364bec5aa4eabc9406af41ee32692e983960880a67b7895e`  
		Last Modified: Thu, 14 Oct 2021 03:18:45 GMT  
		Size: 297.7 MB (297666206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e110d1093fff02b16392aabfa860af93046182bff2efaac6cb6db121786bf`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3d6b6cd6f6f549606ac78ccf9cbae8594264d8d8a6b23b070757140bbe445`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4bcdd07c10eba354b849d6575763ca94cd5bcd04e8b68eab99a6f933d74c4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13028da805d1e9f7af14e427b1da8f471a2a6bb06f8356d9cbfdcaabe497245`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d4997ea504fc935c0e460a2e20f2b34ae860020d2ecc8e101dfa12514cfc4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:67bd3a30bd978a0c6c785753a32fa3959287216bc1fab41d7b976889c89b8ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22264a0e41f5d1bdb578aef073fc0be9e98b87b520c237233e320e219087da73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.9 MB (716866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa444e12f457ad05650c24cf66fd1407d7066e670c6bf9af0280ab54e63f0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:21:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:21:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 08 Oct 2021 23:21:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:21:46 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:21:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:21:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:21:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:21:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ec7855604de4410f6b633da69fc863f74332acab6411ac7726decc4591421`  
		Last Modified: Fri, 08 Oct 2021 23:23:42 GMT  
		Size: 297.7 MB (297665999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b36beadc0e3f9eb2ab9b771d8c50c067a63c85122fa0e247d9b059d211ca01`  
		Last Modified: Fri, 08 Oct 2021 23:23:25 GMT  
		Size: 795.4 KB (795419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04803a6e88ed7004bbdad416bec1782e9fd14dc80753767f0b3943e01123bbfb`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45696640937fd910d83c0057455bab285b7ddd3747fd5f58789999219807f1`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acac556405b1d66473149a0aeeb6d67ce5cdceed14d288b1cb15728441dcc9be`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e5ada93951ebc56fde42c610817441b784bb8184288f296f99a55a68ca3a4`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b5343ba912f4ac7359356079c433b6bfdf9d69895a2fb586e8d115e595714824
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.7 MB (707674973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2aa3a4b8e73028c6b94db8a38da1d5be5691ad5ed17a4106a228bd68f8e401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:14:14 GMT
ENV XWIKI_VERSION=12.10.10
# Thu, 14 Oct 2021 03:14:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Thu, 14 Oct 2021 03:14:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Thu, 14 Oct 2021 03:15:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:15:27 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:15:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:15:29 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:15:30 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:15:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:15:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:15:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c372ded7cdd263364bec5aa4eabc9406af41ee32692e983960880a67b7895e`  
		Last Modified: Thu, 14 Oct 2021 03:18:45 GMT  
		Size: 297.7 MB (297666206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e110d1093fff02b16392aabfa860af93046182bff2efaac6cb6db121786bf`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3d6b6cd6f6f549606ac78ccf9cbae8594264d8d8a6b23b070757140bbe445`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4bcdd07c10eba354b849d6575763ca94cd5bcd04e8b68eab99a6f933d74c4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13028da805d1e9f7af14e427b1da8f471a2a6bb06f8356d9cbfdcaabe497245`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d4997ea504fc935c0e460a2e20f2b34ae860020d2ecc8e101dfa12514cfc4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.10` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:12.10.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:67bd3a30bd978a0c6c785753a32fa3959287216bc1fab41d7b976889c89b8ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22264a0e41f5d1bdb578aef073fc0be9e98b87b520c237233e320e219087da73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.9 MB (716866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa444e12f457ad05650c24cf66fd1407d7066e670c6bf9af0280ab54e63f0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:21:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:21:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 08 Oct 2021 23:21:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:21:46 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:21:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:21:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:21:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:21:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ec7855604de4410f6b633da69fc863f74332acab6411ac7726decc4591421`  
		Last Modified: Fri, 08 Oct 2021 23:23:42 GMT  
		Size: 297.7 MB (297665999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b36beadc0e3f9eb2ab9b771d8c50c067a63c85122fa0e247d9b059d211ca01`  
		Last Modified: Fri, 08 Oct 2021 23:23:25 GMT  
		Size: 795.4 KB (795419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04803a6e88ed7004bbdad416bec1782e9fd14dc80753767f0b3943e01123bbfb`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45696640937fd910d83c0057455bab285b7ddd3747fd5f58789999219807f1`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acac556405b1d66473149a0aeeb6d67ce5cdceed14d288b1cb15728441dcc9be`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e5ada93951ebc56fde42c610817441b784bb8184288f296f99a55a68ca3a4`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b5343ba912f4ac7359356079c433b6bfdf9d69895a2fb586e8d115e595714824
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.7 MB (707674973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2aa3a4b8e73028c6b94db8a38da1d5be5691ad5ed17a4106a228bd68f8e401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:14:14 GMT
ENV XWIKI_VERSION=12.10.10
# Thu, 14 Oct 2021 03:14:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Thu, 14 Oct 2021 03:14:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Thu, 14 Oct 2021 03:15:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:15:27 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:15:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:15:29 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:15:30 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:15:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:15:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:15:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c372ded7cdd263364bec5aa4eabc9406af41ee32692e983960880a67b7895e`  
		Last Modified: Thu, 14 Oct 2021 03:18:45 GMT  
		Size: 297.7 MB (297666206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e110d1093fff02b16392aabfa860af93046182bff2efaac6cb6db121786bf`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3d6b6cd6f6f549606ac78ccf9cbae8594264d8d8a6b23b070757140bbe445`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4bcdd07c10eba354b849d6575763ca94cd5bcd04e8b68eab99a6f933d74c4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13028da805d1e9f7af14e427b1da8f471a2a6bb06f8356d9cbfdcaabe497245`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d4997ea504fc935c0e460a2e20f2b34ae860020d2ecc8e101dfa12514cfc4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4`

```console
$ docker pull xwiki@sha256:9652e04827077fefd331e334e8d672bc0268edc05489edc2a48122f6d0bb88ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4` - linux; amd64

```console
$ docker pull xwiki@sha256:dce469b72c7f6993e631b8bc27bb4c831a5a81f9030711a1d9a82f198bd4381f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.4 MB (723356396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec5b43248d7f2033047adc0064702410fa294dff40518b48fab3dccd190ad7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:03:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:03:48 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 23:03:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:03:51 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:03:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:03:52 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:03:52 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:03:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c62cd19c76ea319fc56b5379bb420973684bf326d3aceefb4df8a714a05c4`  
		Last Modified: Thu, 07 Oct 2021 23:09:05 GMT  
		Size: 303.5 MB (303492853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eddec9787ed03f4c8273116ce8a1bd542f269d1e88177380c138092acb2a37`  
		Last Modified: Thu, 07 Oct 2021 23:08:48 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5d0c5f686abc130e8c10fdc03ebdcd56d04c41eff45c81b3950952e93c5874`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddd17fa0c0095a9f8668716aa7dbf92877e5363a02d8395c356ca670a62d779`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07f31bdd7adca0f6e5f8a805c4646f715a9e72b2171566ed020a9a07457aacf`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a3acac1de70983bce3f77a1c9ca4f8075ba4cf4b6bdd8e647d9e4056d8f3b`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:9652e04827077fefd331e334e8d672bc0268edc05489edc2a48122f6d0bb88ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dce469b72c7f6993e631b8bc27bb4c831a5a81f9030711a1d9a82f198bd4381f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.4 MB (723356396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec5b43248d7f2033047adc0064702410fa294dff40518b48fab3dccd190ad7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:03:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:03:48 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 23:03:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:03:51 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:03:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:03:52 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:03:52 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:03:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c62cd19c76ea319fc56b5379bb420973684bf326d3aceefb4df8a714a05c4`  
		Last Modified: Thu, 07 Oct 2021 23:09:05 GMT  
		Size: 303.5 MB (303492853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eddec9787ed03f4c8273116ce8a1bd542f269d1e88177380c138092acb2a37`  
		Last Modified: Thu, 07 Oct 2021 23:08:48 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5d0c5f686abc130e8c10fdc03ebdcd56d04c41eff45c81b3950952e93c5874`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddd17fa0c0095a9f8668716aa7dbf92877e5363a02d8395c356ca670a62d779`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07f31bdd7adca0f6e5f8a805c4646f715a9e72b2171566ed020a9a07457aacf`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a3acac1de70983bce3f77a1c9ca4f8075ba4cf4b6bdd8e647d9e4056d8f3b`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:8f4436484749eef6bfdf61167595be8533507c0a6ac7125e7ce557e5a107820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f48fee0296348baf723cf79f9c772c6454163581fff87861260ca8aa170bc84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.7 MB (722693478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3686fb9e688a910a032d70956bbabaf7f4959720e8350ab38c1adb481d4af94e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:58 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:59 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:04:39 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:04:40 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:04:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:04:41 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:04:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:04:42 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:04:42 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:04:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:04:42 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d50ae115670c3815d5762fc4cddd612353a74fab18431eb65f4e7b81efae665`  
		Last Modified: Thu, 07 Oct 2021 23:09:39 GMT  
		Size: 303.5 MB (303492836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6ec82cb59c629617ad5022076413df0cbff3c5e438bba98a5caaec28bcf1f`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49cfbd60beebfa57a20a6c7143478f2f8b7802ef56639fa584040c8afff3ede`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d399819e9b95682847d32880ca147fe4e0765fbf83444452e37121666ad1a81`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74019947e83e665226e5d4b10c40ef5c90c0461ef1fdb327ec05fadac089856`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41752b14f0d33eaf005914740b9be3aec5c7f9337676fef9f23361a4fee18e43`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cf0b20570e66e748e5724aa6b8efaba0f2c7581ed194e3b9704e522c79b73d00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.5 MB (713501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5abc34307cbf455c8289f418b3ac59436c1f2e74824ca4cc547a1f48df3f81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:15:41 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 14 Oct 2021 03:15:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 14 Oct 2021 03:15:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 14 Oct 2021 03:16:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:16:52 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:16:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:16:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:16:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:16:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:16:57 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:16:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c904890d06a172b0f4972ac0a82de72be5b3295e7a9465a1ec4958b912b8c1a4`  
		Last Modified: Thu, 14 Oct 2021 03:19:32 GMT  
		Size: 303.5 MB (303492687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd9752bdb96b5357b144163234e50d389160ab9a03bc87d577f1f1066b33e89`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8a1ceb05fbba79a587e1dad7c7d106d240048875239021b779fdacee6bd343`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dba03a4aa08334253fb3603a43d633f3c2c0a9bb1f3bf67ade52ed1b5ae2dc4`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db19dc6d74d619de3a88b6f8b73428cae810e17233309f1dcdabf815ee552a`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018fb478a3d0a7013ccb34603e5d5b54593f611f976e1869ddb7b7dee27b756c`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3`

```console
$ docker pull xwiki@sha256:9652e04827077fefd331e334e8d672bc0268edc05489edc2a48122f6d0bb88ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.3` - linux; amd64

```console
$ docker pull xwiki@sha256:dce469b72c7f6993e631b8bc27bb4c831a5a81f9030711a1d9a82f198bd4381f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.4 MB (723356396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec5b43248d7f2033047adc0064702410fa294dff40518b48fab3dccd190ad7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:03:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:03:48 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 23:03:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:03:51 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:03:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:03:52 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:03:52 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:03:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c62cd19c76ea319fc56b5379bb420973684bf326d3aceefb4df8a714a05c4`  
		Last Modified: Thu, 07 Oct 2021 23:09:05 GMT  
		Size: 303.5 MB (303492853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eddec9787ed03f4c8273116ce8a1bd542f269d1e88177380c138092acb2a37`  
		Last Modified: Thu, 07 Oct 2021 23:08:48 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5d0c5f686abc130e8c10fdc03ebdcd56d04c41eff45c81b3950952e93c5874`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddd17fa0c0095a9f8668716aa7dbf92877e5363a02d8395c356ca670a62d779`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07f31bdd7adca0f6e5f8a805c4646f715a9e72b2171566ed020a9a07457aacf`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a3acac1de70983bce3f77a1c9ca4f8075ba4cf4b6bdd8e647d9e4056d8f3b`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3-mysql-tomcat`

```console
$ docker pull xwiki@sha256:9652e04827077fefd331e334e8d672bc0268edc05489edc2a48122f6d0bb88ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.4.3-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:dce469b72c7f6993e631b8bc27bb4c831a5a81f9030711a1d9a82f198bd4381f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.4 MB (723356396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec5b43248d7f2033047adc0064702410fa294dff40518b48fab3dccd190ad7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:03:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:03:48 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 23:03:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 23:03:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:03:51 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:03:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:03:52 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:03:52 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:03:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3c62cd19c76ea319fc56b5379bb420973684bf326d3aceefb4df8a714a05c4`  
		Last Modified: Thu, 07 Oct 2021 23:09:05 GMT  
		Size: 303.5 MB (303492853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eddec9787ed03f4c8273116ce8a1bd542f269d1e88177380c138092acb2a37`  
		Last Modified: Thu, 07 Oct 2021 23:08:48 GMT  
		Size: 2.3 MB (2257823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5d0c5f686abc130e8c10fdc03ebdcd56d04c41eff45c81b3950952e93c5874`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddd17fa0c0095a9f8668716aa7dbf92877e5363a02d8395c356ca670a62d779`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07f31bdd7adca0f6e5f8a805c4646f715a9e72b2171566ed020a9a07457aacf`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 5.2 KB (5175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146a3acac1de70983bce3f77a1c9ca4f8075ba4cf4b6bdd8e647d9e4056d8f3b`  
		Last Modified: Thu, 07 Oct 2021 23:08:47 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.4.3-postgres-tomcat`

```console
$ docker pull xwiki@sha256:8f4436484749eef6bfdf61167595be8533507c0a6ac7125e7ce557e5a107820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.4.3-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f48fee0296348baf723cf79f9c772c6454163581fff87861260ca8aa170bc84f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.7 MB (722693478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3686fb9e688a910a032d70956bbabaf7f4959720e8350ab38c1adb481d4af94e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:03:58 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 07 Oct 2021 23:03:58 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 07 Oct 2021 23:03:59 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 07 Oct 2021 23:04:39 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:04:40 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:04:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:04:41 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:04:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:04:42 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:04:42 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:04:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:04:42 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d50ae115670c3815d5762fc4cddd612353a74fab18431eb65f4e7b81efae665`  
		Last Modified: Thu, 07 Oct 2021 23:09:39 GMT  
		Size: 303.5 MB (303492836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f6ec82cb59c629617ad5022076413df0cbff3c5e438bba98a5caaec28bcf1f`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49cfbd60beebfa57a20a6c7143478f2f8b7802ef56639fa584040c8afff3ede`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d399819e9b95682847d32880ca147fe4e0765fbf83444452e37121666ad1a81`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74019947e83e665226e5d4b10c40ef5c90c0461ef1fdb327ec05fadac089856`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41752b14f0d33eaf005914740b9be3aec5c7f9337676fef9f23361a4fee18e43`  
		Last Modified: Thu, 07 Oct 2021 23:09:22 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.4.3-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cf0b20570e66e748e5724aa6b8efaba0f2c7581ed194e3b9704e522c79b73d00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.5 MB (713501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5abc34307cbf455c8289f418b3ac59436c1f2e74824ca4cc547a1f48df3f81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:15:41 GMT
ENV XWIKI_VERSION=13.4.3
# Thu, 14 Oct 2021 03:15:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4.3
# Thu, 14 Oct 2021 03:15:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=cf075d7643b941721dbb197122ae7ba5bc05ff9d02595a6b0d8b1335f920a1fb
# Thu, 14 Oct 2021 03:16:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:16:52 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:16:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:16:55 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:16:56 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:16:57 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:16:57 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:16:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:16:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c904890d06a172b0f4972ac0a82de72be5b3295e7a9465a1ec4958b912b8c1a4`  
		Last Modified: Thu, 14 Oct 2021 03:19:32 GMT  
		Size: 303.5 MB (303492687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd9752bdb96b5357b144163234e50d389160ab9a03bc87d577f1f1066b33e89`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 795.4 KB (795415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8a1ceb05fbba79a587e1dad7c7d106d240048875239021b779fdacee6bd343`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dba03a4aa08334253fb3603a43d633f3c2c0a9bb1f3bf67ade52ed1b5ae2dc4`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db19dc6d74d619de3a88b6f8b73428cae810e17233309f1dcdabf815ee552a`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018fb478a3d0a7013ccb34603e5d5b54593f611f976e1869ddb7b7dee27b756c`  
		Last Modified: Thu, 14 Oct 2021 03:19:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.8` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.8-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.8-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.8-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8.0`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.8.0` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:13.8.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.8.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.8.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.8.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:239db5cc0a71574282457e05e6d62b1f94ad155aae1192ff6a4701f8580fc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4fcc541ba9cfd207790737cd5f483c44e3b7e93bb7e34f07ebeae32e5e8589c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.5 MB (717529583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8315f96b31f3f81b216207fd3162292592e49da882f2d37e0aac5629dd8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:20:13 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:20:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:20:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:20:55 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:56 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Fri, 08 Oct 2021 23:20:57 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 08 Oct 2021 23:20:57 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:20:58 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:20:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:20:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:20:59 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:20:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8642be3871d54a58a844225e30b146ba88dcaf29aa101982b22fa09d0eccdd`  
		Last Modified: Fri, 08 Oct 2021 23:22:53 GMT  
		Size: 297.7 MB (297665998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6cef98e22008224722a798b7854a567527cd2f2bdfad4f38c6d5a6da2bef9`  
		Last Modified: Fri, 08 Oct 2021 23:22:36 GMT  
		Size: 2.3 MB (2257812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144a3fa7aaf40278285244963a83392f93368287eb9da8969f7c9e0ae1b5948`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaacc860279a3600544079b796ed67dab840f8591073cd3c7166355e77d05d7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9c67cf9f57d05aed3b132a16e22304eb478cb2b38ca96771875c6f72f5749`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d0c714b4de4800ca317788247648e5ed4807a4724494b828f0206aada445f7`  
		Last Modified: Fri, 08 Oct 2021 23:22:35 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:67bd3a30bd978a0c6c785753a32fa3959287216bc1fab41d7b976889c89b8ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:22264a0e41f5d1bdb578aef073fc0be9e98b87b520c237233e320e219087da73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.9 MB (716866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa444e12f457ad05650c24cf66fd1407d7066e670c6bf9af0280ab54e63f0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:21:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:21:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 08 Oct 2021 23:21:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:21:46 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:21:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:21:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:21:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:21:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ec7855604de4410f6b633da69fc863f74332acab6411ac7726decc4591421`  
		Last Modified: Fri, 08 Oct 2021 23:23:42 GMT  
		Size: 297.7 MB (297665999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b36beadc0e3f9eb2ab9b771d8c50c067a63c85122fa0e247d9b059d211ca01`  
		Last Modified: Fri, 08 Oct 2021 23:23:25 GMT  
		Size: 795.4 KB (795419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04803a6e88ed7004bbdad416bec1782e9fd14dc80753767f0b3943e01123bbfb`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45696640937fd910d83c0057455bab285b7ddd3747fd5f58789999219807f1`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acac556405b1d66473149a0aeeb6d67ce5cdceed14d288b1cb15728441dcc9be`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e5ada93951ebc56fde42c610817441b784bb8184288f296f99a55a68ca3a4`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b5343ba912f4ac7359356079c433b6bfdf9d69895a2fb586e8d115e595714824
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.7 MB (707674973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2aa3a4b8e73028c6b94db8a38da1d5be5691ad5ed17a4106a228bd68f8e401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:14:14 GMT
ENV XWIKI_VERSION=12.10.10
# Thu, 14 Oct 2021 03:14:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Thu, 14 Oct 2021 03:14:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Thu, 14 Oct 2021 03:15:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:15:27 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:15:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:15:29 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:15:30 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:15:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:15:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:15:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c372ded7cdd263364bec5aa4eabc9406af41ee32692e983960880a67b7895e`  
		Last Modified: Thu, 14 Oct 2021 03:18:45 GMT  
		Size: 297.7 MB (297666206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e110d1093fff02b16392aabfa860af93046182bff2efaac6cb6db121786bf`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3d6b6cd6f6f549606ac78ccf9cbae8594264d8d8a6b23b070757140bbe445`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4bcdd07c10eba354b849d6575763ca94cd5bcd04e8b68eab99a6f933d74c4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13028da805d1e9f7af14e427b1da8f471a2a6bb06f8356d9cbfdcaabe497245`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d4997ea504fc935c0e460a2e20f2b34ae860020d2ecc8e101dfa12514cfc4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:67bd3a30bd978a0c6c785753a32fa3959287216bc1fab41d7b976889c89b8ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22264a0e41f5d1bdb578aef073fc0be9e98b87b520c237233e320e219087da73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.9 MB (716866685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa444e12f457ad05650c24cf66fd1407d7066e670c6bf9af0280ab54e63f0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_VERSION=12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Fri, 08 Oct 2021 23:21:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Fri, 08 Oct 2021 23:21:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 08 Oct 2021 23:21:45 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 08 Oct 2021 23:21:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 08 Oct 2021 23:21:46 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 08 Oct 2021 23:21:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 08 Oct 2021 23:21:47 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 08 Oct 2021 23:21:47 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Oct 2021 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:21:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ec7855604de4410f6b633da69fc863f74332acab6411ac7726decc4591421`  
		Last Modified: Fri, 08 Oct 2021 23:23:42 GMT  
		Size: 297.7 MB (297665999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b36beadc0e3f9eb2ab9b771d8c50c067a63c85122fa0e247d9b059d211ca01`  
		Last Modified: Fri, 08 Oct 2021 23:23:25 GMT  
		Size: 795.4 KB (795419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04803a6e88ed7004bbdad416bec1782e9fd14dc80753767f0b3943e01123bbfb`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e45696640937fd910d83c0057455bab285b7ddd3747fd5f58789999219807f1`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acac556405b1d66473149a0aeeb6d67ce5cdceed14d288b1cb15728441dcc9be`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e5ada93951ebc56fde42c610817441b784bb8184288f296f99a55a68ca3a4`  
		Last Modified: Fri, 08 Oct 2021 23:23:24 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b5343ba912f4ac7359356079c433b6bfdf9d69895a2fb586e8d115e595714824
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.7 MB (707674973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2aa3a4b8e73028c6b94db8a38da1d5be5691ad5ed17a4106a228bd68f8e401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:14:14 GMT
ENV XWIKI_VERSION=12.10.10
# Thu, 14 Oct 2021 03:14:15 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.10
# Thu, 14 Oct 2021 03:14:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=42364fd6a3d575c78969ebb12a7d28360ccff3b478379cf30232d6611ccbe9e0
# Thu, 14 Oct 2021 03:15:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:15:27 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:15:28 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:15:29 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:15:30 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:15:31 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:15:31 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:15:33 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c372ded7cdd263364bec5aa4eabc9406af41ee32692e983960880a67b7895e`  
		Last Modified: Thu, 14 Oct 2021 03:18:45 GMT  
		Size: 297.7 MB (297666206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e110d1093fff02b16392aabfa860af93046182bff2efaac6cb6db121786bf`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 795.4 KB (795423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd3d6b6cd6f6f549606ac78ccf9cbae8594264d8d8a6b23b070757140bbe445`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4bcdd07c10eba354b849d6575763ca94cd5bcd04e8b68eab99a6f933d74c4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13028da805d1e9f7af14e427b1da8f471a2a6bb06f8356d9cbfdcaabe497245`  
		Last Modified: Thu, 14 Oct 2021 03:18:23 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d4997ea504fc935c0e460a2e20f2b34ae860020d2ecc8e101dfa12514cfc4`  
		Last Modified: Thu, 14 Oct 2021 03:18:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8f8e36b0e7d12e120ad7d6c27c788883a7d9266c07555fb43a1a1a3df117d044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:39f03f7ba16115a766e320b45431d4337cb909698183a25debd374018645d8ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706609096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae40e76d25d59f60bd95b13f78c5ca87542491d0670c4fdcdd0d521b89e51f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 22:59:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 22:59:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 22:59:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 22:59:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 22:59:51 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:52 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Thu, 07 Oct 2021 22:59:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Thu, 07 Oct 2021 22:59:53 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 22:59:54 GMT
COPY file:f575763e48b0a178418336ca6a3d69292305cd0be2b14b7d744d036857f245b8 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 22:59:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 22:59:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 22:59:55 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 22:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:59:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b623bb959185bf81d4210251d34338af7e401a21e2ff48b295bd3e4cbfaa936`  
		Last Modified: Thu, 07 Oct 2021 23:05:53 GMT  
		Size: 167.5 MB (167472617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cad84661cef546755403192a8be2e87a61c129f547c5115784f86dea5382d7`  
		Last Modified: Thu, 07 Oct 2021 23:05:46 GMT  
		Size: 286.7 MB (286745412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac658c207d012d8f6510af6001e43662bdbb9a327978daf0fc08a67109639138`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.3 MB (2257825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc03d20407180a4d98e7f3e37580bd662e7453dc7790701013fcf6b5da2b5f`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6687b4192c515f3cc90a5d3d369ea7e0d8d410732c4507b9a574ec58940261c`  
		Last Modified: Thu, 07 Oct 2021 23:05:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223bd06b8321c45f84ac602b63aaa7f0812784630e7602a6b7ffa5e5482a4063`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac49a7326cfec91723c37c4e4232b4294e9f04c436747b903f59e0c4be30707`  
		Last Modified: Thu, 07 Oct 2021 23:05:27 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5a9ec5dd667ce28d6531c82bfa77633ff475c2c8faf9f06ef3422874c3859057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:0aa92f520ff7ecf88eacbe4440e3f35122954b432ab026baf294e94426fedc19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.9 MB (705946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eac6593890fe8b5c5da198f7f52e67d05e49d67295e6eab43399f576cf0f8eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
# Fri, 01 Oct 2021 08:57:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 01 Oct 2021 08:57:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 08:57:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 01 Oct 2021 08:57:47 GMT
WORKDIR /usr/local/tomcat
# Fri, 01 Oct 2021 08:57:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 08:57:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 01 Oct 2021 09:12:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 01 Oct 2021 09:12:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_VERSION=8.5.72
# Thu, 07 Oct 2021 20:35:10 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Thu, 07 Oct 2021 20:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 07 Oct 2021 20:35:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 07 Oct 2021 20:35:46 GMT
EXPOSE 8080
# Thu, 07 Oct 2021 20:35:46 GMT
CMD ["catalina.sh" "run"]
# Thu, 07 Oct 2021 22:57:05 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 07 Oct 2021 23:00:34 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_VERSION=13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 07 Oct 2021 23:00:35 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 07 Oct 2021 23:01:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 07 Oct 2021 23:01:15 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 07 Oct 2021 23:01:15 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 07 Oct 2021 23:01:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 07 Oct 2021 23:01:17 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 07 Oct 2021 23:01:17 GMT
VOLUME [/usr/local/xwiki]
# Thu, 07 Oct 2021 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:01:17 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce3c749dcb4970567ee80c11c3a340d848976522a3dac00b12afddb095e7289`  
		Last Modified: Fri, 01 Oct 2021 09:26:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec3e025270c2ee246c6e30ed6d5b3af20878c55d4d9dfa2b5adce06dd48a17`  
		Last Modified: Thu, 07 Oct 2021 21:06:08 GMT  
		Size: 11.7 MB (11706810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31886fd79fe04834536b8fcc77ec683029a6a972113bcbd8d2f728069f7da54`  
		Last Modified: Thu, 07 Oct 2021 21:06:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ddce4ddd7d719d83cde1cd69f9d374c0cc965330e3c2297f6f7b7e25a4e055`  
		Last Modified: Thu, 07 Oct 2021 23:06:58 GMT  
		Size: 168.3 MB (168271971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65d318ead32e71f7ba0b294d03af7034340d46afbd62d3c29d94d1e0f559f3`  
		Last Modified: Thu, 07 Oct 2021 23:06:50 GMT  
		Size: 286.7 MB (286745534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95272f28697eac37a7459dc01087c98c50361e20da62cf968456b82c0f2772d6`  
		Last Modified: Thu, 07 Oct 2021 23:06:32 GMT  
		Size: 795.4 KB (795426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb5d1487611f2467cd57428988c26958dfb3e159bd558924e04aa13b04bf3d`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee6ef68aa34a1975dbfa8771f5edaa37ec43f9a61431c3f1ecba091cff9b780`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586ce62132661b22fb775ca0ed771136d9e2f60f6eae50b064e9e3bb80045594`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0f814b3f14eb0a0c4fae6bf4cb1df845fcd5b65aa6c4de9bce7316a8e0098b`  
		Last Modified: Thu, 07 Oct 2021 23:06:31 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d526333d602769d5d499614b4ca8b7bd1928579bbc1eaab9c8c70f27fc4e4d80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696754183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433a4aa13a9a9efbe97d80a97747b04720f0ce5a78ec037cbdf3ee9d773186f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 08:42:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:42:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:42:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:42:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:42:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:42:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 09:43:06 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 13 Oct 2021 09:43:07 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Oct 2021 09:43:08 GMT
ENV TOMCAT_VERSION=8.5.72
# Wed, 13 Oct 2021 09:43:09 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Wed, 13 Oct 2021 09:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 13 Oct 2021 09:43:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 09:43:54 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 09:43:55 GMT
CMD ["catalina.sh" "run"]
# Thu, 14 Oct 2021 03:12:15 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 14 Oct 2021 03:12:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_VERSION=13.8
# Thu, 14 Oct 2021 03:12:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.8
# Thu, 14 Oct 2021 03:12:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=893acafbe88ad863fffa8f29a33984366bba532e18cf421946320775e95ff12f
# Thu, 14 Oct 2021 03:14:00 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 14 Oct 2021 03:14:01 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 14 Oct 2021 03:14:02 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 14 Oct 2021 03:14:03 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 14 Oct 2021 03:14:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 14 Oct 2021 03:14:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Oct 2021 03:14:05 GMT
VOLUME [/usr/local/xwiki]
# Thu, 14 Oct 2021 03:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Oct 2021 03:14:07 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ec82d1f49de36c90393c61343fe392b0863f82e8e50cc66a1db4ba431551ce`  
		Last Modified: Wed, 13 Oct 2021 10:21:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbeb90d32a072ee7944b6a56719bbf325992d509c0e5103be1f8315cb9dd541`  
		Last Modified: Wed, 13 Oct 2021 10:58:59 GMT  
		Size: 11.5 MB (11488652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0a00a33a74283a4ef0a914d87d2ea2594b83be06fcb28b4e7f6dd23d538133`  
		Last Modified: Thu, 14 Oct 2021 03:17:57 GMT  
		Size: 164.1 MB (164143426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c24c654cd894a516c1862c9e8e332328f6b0f177d498d609a576a96c93dda9a`  
		Last Modified: Thu, 14 Oct 2021 03:17:55 GMT  
		Size: 286.7 MB (286745322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43bab1f44494617377bc4ea8b4c1a66bb146bd862ba92c4d398c72174f6328`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 795.4 KB (795421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a215a3ddd36bdb5b4920a45ed86cde139e413601f6e4274a3514085a181a71`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e47b853f20cbee87a5b83c8f8bb88d5116c416bb81051a9e34cab1c784f69`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb846cfedf94d39ee1778d3c3c72b489cb81ccb7726b4dfab25a5972fe09fd95`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 5.3 KB (5322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30507f3a0f64177628bf3b1850f010233a6fbb7001db73623cf6ca136993c3f`  
		Last Modified: Thu, 14 Oct 2021 03:17:33 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
