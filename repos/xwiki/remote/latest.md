## `xwiki:latest`

```console
$ docker pull xwiki@sha256:a2c4f623d8174b0c2fdad057e015932ba34baec3a7514f6c8ad69bda3f3ef071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:3d115b9ed326ca8e15743405f6b925056d629b2b12655d94c4b4f5687326730b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 MB (637593293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a943046ffdf073df50f1e1ad99f0a1d31bae8c95ec5d9ad8da67b312187e63a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 15:47:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:47:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 15:47:29 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 15:47:29 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 15:47:29 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:28:07 GMT
ENV JAVA_VERSION=11.0.16
# Mon, 25 Jul 2022 20:28:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Jul 2022 23:09:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 23:09:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 23:09:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 23:09:41 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 23:09:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:09:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:16:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Jul 2022 23:16:18 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Jul 2022 23:16:18 GMT
ENV TOMCAT_VERSION=9.0.65
# Mon, 25 Jul 2022 23:16:18 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Mon, 25 Jul 2022 23:16:19 GMT
COPY dir:72a6b2f810555478cfa1d75e94ad553add3571bc6014f31867f07702411cbb5a in /usr/local/tomcat 
# Mon, 25 Jul 2022 23:16:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Jul 2022 23:16:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Jul 2022 23:16:24 GMT
EXPOSE 8080
# Mon, 25 Jul 2022 23:16:24 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 26 Jul 2022 00:51:35 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 26 Jul 2022 00:52:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 00:52:14 GMT
ENV XWIKI_VERSION=14.6
# Tue, 26 Jul 2022 00:52:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.6
# Tue, 26 Jul 2022 00:52:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=9676cc9eeae3cf47bccae037bff67ce2468e3bec1d126f903b4d3fe61bff8723
# Tue, 26 Jul 2022 00:52:52 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 26 Jul 2022 00:52:53 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Tue, 26 Jul 2022 00:52:53 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Tue, 26 Jul 2022 00:52:53 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Tue, 26 Jul 2022 00:52:53 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Tue, 26 Jul 2022 00:52:53 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Tue, 26 Jul 2022 00:52:54 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 26 Jul 2022 00:52:54 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 26 Jul 2022 00:52:54 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 26 Jul 2022 00:52:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 26 Jul 2022 00:52:55 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 26 Jul 2022 00:52:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 26 Jul 2022 00:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 00:52:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19babefbed0663644efc4f2bc7bc5ae6914628808e42cd7dae490844da02ef4a`  
		Last Modified: Tue, 12 Jul 2022 16:00:07 GMT  
		Size: 5.7 MB (5657891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529e95713a10aa41fdb7a9f2a610a4c32b721b77d74f3c1e6aadec5170a893db`  
		Last Modified: Tue, 12 Jul 2022 16:00:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956f2f36dfb2b2629ab92608a3737feb92c98d7bd4ad40a6e2820362bd32e66b`  
		Last Modified: Mon, 25 Jul 2022 20:40:50 GMT  
		Size: 45.8 MB (45769248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af8fbbe689577d47ddbb27e4fe4b72d10454452e8ba2a0c0ae2039c645c0d93`  
		Last Modified: Mon, 25 Jul 2022 23:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1844fc3636b7287f28031d80db992be8b8aca238a3221229d30973abd3b8770`  
		Last Modified: Mon, 25 Jul 2022 23:44:24 GMT  
		Size: 12.2 MB (12160309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b948b6d231d0d8e60eb07f8df5bebe5e6b4161ce58c5b12eb8a4f798c9da9a`  
		Last Modified: Mon, 25 Jul 2022 23:44:23 GMT  
		Size: 459.7 KB (459730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71387be9557aa79eb3d963fa85977a78e812ecb9a5fba842f16c38703776961`  
		Last Modified: Mon, 25 Jul 2022 23:44:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac69536873246f7a29ea24de2b90a0182b0ecad61505d0005b7bc7f796e11e1f`  
		Last Modified: Tue, 26 Jul 2022 00:59:15 GMT  
		Size: 200.2 MB (200196648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03e738a771a4195b36c4f2dc95c5784053cd785c3cce5eb2d7694eb99a1854`  
		Last Modified: Tue, 26 Jul 2022 00:59:01 GMT  
		Size: 299.9 MB (299923830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885a10be09224421de41c794dfee8a9018f6e401b4c71682b66785d7a36a749a`  
		Last Modified: Tue, 26 Jul 2022 00:58:42 GMT  
		Size: 2.4 MB (2381169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45448bb2703662d5a71be44296568b1a4336b1beb1bf0d47f0f4578d6e5d9c08`  
		Last Modified: Tue, 26 Jul 2022 00:58:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc0feadd1dc5527c7828ab06e2c493a6db8572b5844b0205143a8f9cdcdd8c2`  
		Last Modified: Tue, 26 Jul 2022 00:58:41 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b20b4d679ecca74db7f34029c6f016acc103efc8edb51278fe22357b5603aeb`  
		Last Modified: Tue, 26 Jul 2022 00:58:41 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940469685aa26f1778aa93f96f6182d1cf7361a28355b155f75f3e9a0fa2f4bd`  
		Last Modified: Tue, 26 Jul 2022 00:58:41 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a466fbc65f17000f676c7ccc6427b28eabea528549ecbcb86b2e8911f0fe4d93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.1 MB (630148490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eafee2dc4df747ea07acb33f3cc19793cca0e29378284774954aa9383418009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 16:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 16:45:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 16:45:17 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 16:45:18 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 16:45:19 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:55:16 GMT
ENV JAVA_VERSION=11.0.16
# Mon, 25 Jul 2022 20:55:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Jul 2022 22:46:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 22:46:33 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 22:46:34 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 22:46:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 22:46:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 22:46:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 22:57:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Jul 2022 22:57:25 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Jul 2022 22:57:26 GMT
ENV TOMCAT_VERSION=9.0.65
# Mon, 25 Jul 2022 22:57:27 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Mon, 25 Jul 2022 22:57:29 GMT
COPY dir:059248f08f53074e1160790c44bfa2640b6ff7900afa307c184717fd1cafda65 in /usr/local/tomcat 
# Mon, 25 Jul 2022 22:57:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Jul 2022 22:57:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Jul 2022 22:57:34 GMT
EXPOSE 8080
# Mon, 25 Jul 2022 22:57:35 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 Jul 2022 01:35:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 26 Jul 2022 01:35:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 26 Jul 2022 01:35:15 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 26 Jul 2022 01:35:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 26 Jul 2022 01:35:17 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 26 Jul 2022 01:35:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 26 Jul 2022 01:35:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 01:35:50 GMT
ENV XWIKI_VERSION=14.6
# Tue, 26 Jul 2022 01:35:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.6
# Tue, 26 Jul 2022 01:35:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=9676cc9eeae3cf47bccae037bff67ce2468e3bec1d126f903b4d3fe61bff8723
# Tue, 26 Jul 2022 01:36:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 26 Jul 2022 01:36:24 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Tue, 26 Jul 2022 01:36:25 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Tue, 26 Jul 2022 01:36:26 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Tue, 26 Jul 2022 01:36:27 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Tue, 26 Jul 2022 01:36:27 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Tue, 26 Jul 2022 01:36:29 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Tue, 26 Jul 2022 01:36:30 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 26 Jul 2022 01:36:31 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 26 Jul 2022 01:36:32 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 26 Jul 2022 01:36:33 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 26 Jul 2022 01:36:33 GMT
VOLUME [/usr/local/xwiki]
# Tue, 26 Jul 2022 01:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 01:36:35 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60047e9914e670a899370adf2dd0fa2454a135151f9b3a2b871f18ef9e193bce`  
		Last Modified: Tue, 12 Jul 2022 17:04:52 GMT  
		Size: 5.6 MB (5648704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe81dbfbe8d8bda9067737340106f1de9bfae84dda03edf2640783c25345ef2`  
		Last Modified: Tue, 12 Jul 2022 17:04:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f4917b3a622c1c72fd6a59682fa52c5a46bf90a7bc937b7f8afad2ec042eab`  
		Last Modified: Mon, 25 Jul 2022 21:13:48 GMT  
		Size: 45.1 MB (45070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87024ffaf0ab687ff6650d13cce94086f1e6cd57203cf5b360662075b44ea15`  
		Last Modified: Mon, 25 Jul 2022 23:33:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeeb39db3196d973fb6052926704560265ba85b7c85cc7a91c8030d715ae919`  
		Last Modified: Mon, 25 Jul 2022 23:40:57 GMT  
		Size: 12.2 MB (12170160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c43e8ed3866c54c631cc08e4b743a9c562954a155f030547435d747ba1a5cd`  
		Last Modified: Mon, 25 Jul 2022 23:40:56 GMT  
		Size: 217.2 KB (217196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02850df55f43c178242804a93e72d37887d710185bf3478a17e9ddbd5e165937`  
		Last Modified: Tue, 26 Jul 2022 01:44:20 GMT  
		Size: 195.2 MB (195240641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911d4efb3ecf58e29196a668437ef9348ee3340bb21061a59b35ad0c30ae411b`  
		Last Modified: Tue, 26 Jul 2022 01:44:15 GMT  
		Size: 299.9 MB (299923944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5552c4b3648dcbeeba6eed0ff654dc08f0d36ed9e409b22ff6e2e3544ce68b2`  
		Last Modified: Tue, 26 Jul 2022 01:43:52 GMT  
		Size: 2.4 MB (2381173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500f71a845405897e82d6bb8b19b0dd5f9b21678f4752e3f0293f25e0887ddc8`  
		Last Modified: Tue, 26 Jul 2022 01:43:52 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b6c2db380133fc002d1194628da84e7ff3ceac050f33825a33ce3240578d4c`  
		Last Modified: Tue, 26 Jul 2022 01:43:52 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c0c9ff10296b35c51a6bdf8ccd8bbb33d36ddd4f0477cf6a07a38c6a62d53`  
		Last Modified: Tue, 26 Jul 2022 01:43:52 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c352e9e8d9951f9fcca06539b67129add9e1b0a5f5ff27ab053bff3acfa17`  
		Last Modified: Tue, 26 Jul 2022 01:43:52 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
