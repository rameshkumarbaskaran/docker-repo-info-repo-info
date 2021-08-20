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
