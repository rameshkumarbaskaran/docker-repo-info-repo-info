## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:a2af5cb2f66a6d5d38dcc2d843aa26fc9040f37b3482a8537b2397a56cca17e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7f6ffec3d12cd311ee0ea72aec6d99e5604381067af50b83f2a2e45409e87136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.1 MB (631067149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c39796ac1f56ff3e1953d9c3d93709c1df89d2051e61c5a9d9802c064d19d3`
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
# Tue, 12 Jul 2022 15:47:29 GMT
ENV JAVA_VERSION=11.0.15
# Tue, 12 Jul 2022 15:47:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Tue, 12 Jul 2022 18:47:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 Jul 2022 18:47:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:47:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 12 Jul 2022 18:47:52 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 Jul 2022 18:47:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:47:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:57:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 12 Jul 2022 18:57:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 Jul 2022 18:57:43 GMT
ENV TOMCAT_VERSION=9.0.64
# Tue, 12 Jul 2022 18:57:43 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Tue, 12 Jul 2022 18:57:44 GMT
COPY dir:a3067b9f5127e653c5d8a955714495e1eda9c6b54c399ed0809de87baf13f1e1 in /usr/local/tomcat 
# Tue, 12 Jul 2022 18:57:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:57:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 12 Jul 2022 18:57:49 GMT
EXPOSE 8080
# Tue, 12 Jul 2022 18:57:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 Jul 2022 07:15:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 Jul 2022 07:15:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 Jul 2022 07:15:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 Jul 2022 07:15:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 Jul 2022 07:15:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 Jul 2022 07:15:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 Jul 2022 07:17:36 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 13 Jul 2022 07:19:25 GMT
ENV XWIKI_VERSION=13.10.7
# Wed, 13 Jul 2022 07:19:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Wed, 13 Jul 2022 07:19:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Wed, 13 Jul 2022 07:20:02 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 13 Jul 2022 07:20:04 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 13 Jul 2022 07:20:04 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 13 Jul 2022 07:20:04 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 13 Jul 2022 07:20:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 13 Jul 2022 07:20:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 13 Jul 2022 07:20:05 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 Jul 2022 07:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Jul 2022 07:20:06 GMT
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
	-	`sha256:72f9b148e5a2526dcc37b18c4577fd015341d9aed925c43c93acf701ab0430c2`  
		Last Modified: Tue, 12 Jul 2022 16:00:14 GMT  
		Size: 47.2 MB (47197509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15c96d3787ab879ce4a79980c8b2b0616b35bd6e08fbf185e01ce5fe7a53881`  
		Last Modified: Tue, 12 Jul 2022 19:18:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5164dadc69b066339d9515b6ad1b0b5c63c4ad9389862c32d5fcbe687885e743`  
		Last Modified: Tue, 12 Jul 2022 19:28:35 GMT  
		Size: 12.2 MB (12157814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535ed3d04bcb59a375928b5c26eb5214e91cf248d3841a9ad0045d4fa32fc672`  
		Last Modified: Tue, 12 Jul 2022 19:28:34 GMT  
		Size: 459.7 KB (459696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5eb9a4f18d924a66aa717df0e5d58163d31d2b07ec6db159fb6c3c77cb315f`  
		Last Modified: Tue, 12 Jul 2022 19:28:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c7a5cc9fd8ad7963a9719c346ff0fe5d22b943a61dc6d8c8601160174de7dd`  
		Last Modified: Wed, 13 Jul 2022 07:22:46 GMT  
		Size: 201.1 MB (201062676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311432090cf802dce5613a2d442ae3886ab2f4cacefe0ad83202be191d1a396a`  
		Last Modified: Wed, 13 Jul 2022 07:24:49 GMT  
		Size: 292.6 MB (292641288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab16433978cabd65e9c7251e9cb985ab005a94d89a6c4a9b8951057f49c29e`  
		Last Modified: Wed, 13 Jul 2022 07:24:31 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee399a1f218cb6750de2bd37580f50527fb504a8ab6b2d56b63d577e02e3edf`  
		Last Modified: Wed, 13 Jul 2022 07:24:31 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04a4b08ec23f01e5281b5cdc15aebe92fbf7a1735c2db880d9fd1119d5f6e7a`  
		Last Modified: Wed, 13 Jul 2022 07:24:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dd6c003eba0eddea0d2c7a0bd7ec24dde6de26ead53114087188d6a7861006`  
		Last Modified: Wed, 13 Jul 2022 07:24:31 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8544f478ce02d33af8f244b4a77cf90ca84ee45a4d3b5c0f7f8e2d57885a17f5`  
		Last Modified: Wed, 13 Jul 2022 07:24:31 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:32563781213aa9bef6944ce75381b3dcde0e8633e44debf5360f7c409d6723be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.4 MB (623422471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a521d448eeb2c9b441e7287f20270200c96661908a4c65fd7acf40743a75c860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:28 GMT
ADD file:64c455af1bb18ff2c202a244e058b6e5ac147b89410ed36edc5e29f4b6f02c5d in / 
# Thu, 23 Jun 2022 00:40:29 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:23:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Jun 2022 15:23:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:23:05 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:23:06 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:23:07 GMT
ENV JAVA_VERSION=11.0.15
# Thu, 23 Jun 2022 15:23:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 24 Jun 2022 02:32:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 24 Jun 2022 02:32:13 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 02:32:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 24 Jun 2022 02:32:15 GMT
WORKDIR /usr/local/tomcat
# Fri, 24 Jun 2022 02:32:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:32:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:47:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 24 Jun 2022 02:47:06 GMT
ENV TOMCAT_MAJOR=9
# Fri, 24 Jun 2022 02:47:07 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 24 Jun 2022 02:47:08 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 24 Jun 2022 02:47:10 GMT
COPY dir:3cd47eb998163732f948efe2641dc08adb60550a1b3e5b217b7519edbfe89b52 in /usr/local/tomcat 
# Fri, 24 Jun 2022 02:47:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 02:47:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 24 Jun 2022 02:47:16 GMT
EXPOSE 8080
# Fri, 24 Jun 2022 02:47:17 GMT
CMD ["catalina.sh" "run"]
# Mon, 11 Jul 2022 22:47:15 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 11 Jul 2022 22:47:15 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 11 Jul 2022 22:47:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 11 Jul 2022 22:47:17 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 11 Jul 2022 22:47:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 11 Jul 2022 22:47:19 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 11 Jul 2022 22:49:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:52:23 GMT
ENV XWIKI_VERSION=13.10.7
# Mon, 11 Jul 2022 22:52:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.10.7
# Mon, 11 Jul 2022 22:52:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=b886e886ed34e8d7bea8feb2e74e94edb3fb88030f90ab68c7bbc87dcf453d00
# Mon, 11 Jul 2022 22:53:07 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 11 Jul 2022 22:53:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Mon, 11 Jul 2022 22:53:10 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 11 Jul 2022 22:53:11 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 11 Jul 2022 22:53:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 11 Jul 2022 22:53:13 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 11 Jul 2022 22:53:13 GMT
VOLUME [/usr/local/xwiki]
# Mon, 11 Jul 2022 22:53:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jul 2022 22:53:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:f873dfbc59b181817d5bc2b9fc31d90d8f9139c8cabb2fa7264f9bd7b418b8d2`  
		Last Modified: Thu, 23 Jun 2022 00:46:51 GMT  
		Size: 53.7 MB (53696815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b65e0e9cdc28c8cedaabbc5cbae4652c9b107c47684de49f01a77741a5ded`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 4.9 MB (4938760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43836e7983cba8b758620a218a0ee622daf5513308b6a9e8316f94c271ecafd`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 10.7 MB (10656970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1d06b8e25e46c71e32c7364495bbd08b14643238b8910969df33b87769e5db`  
		Last Modified: Thu, 23 Jun 2022 15:50:44 GMT  
		Size: 5.6 MB (5649772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9655f65ff5b77a45459c848ef24050f866d1abdb433646feda7d82539d9e709`  
		Last Modified: Thu, 23 Jun 2022 15:50:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9231830d2e9b0a045a9da49fdc536f6646b7d39688fd6a9fd87f6ca1819b12b2`  
		Last Modified: Thu, 23 Jun 2022 15:50:51 GMT  
		Size: 46.5 MB (46500688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745daea8e1809cc01aa574f9a4820867f78970c9bb58a8786285380aee8653d2`  
		Last Modified: Fri, 24 Jun 2022 03:19:06 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f67a5ca22d499de5b8b8ac0f3d1d6324e45b96ca00ec95e7396bd8c0998dd89`  
		Last Modified: Fri, 24 Jun 2022 03:31:23 GMT  
		Size: 12.2 MB (12167294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d5fcc140e341bd6016843231a2a741d3f07d52b829c9a5e350d3060b7fb11e`  
		Last Modified: Fri, 24 Jun 2022 03:31:21 GMT  
		Size: 217.2 KB (217193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69fe0d7e5812d6720f61027fe7565586da48502ac1c716200360fb752ff9020`  
		Last Modified: Mon, 11 Jul 2022 22:56:49 GMT  
		Size: 196.1 MB (196095321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b708c74492c1768e90941c6dc224352add0e0c0dbb4eb9d57a520349b61350`  
		Last Modified: Mon, 11 Jul 2022 22:59:15 GMT  
		Size: 292.6 MB (292641468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f3faceeb871be5dae712b7050b3a8b6f0abb0e49f0b53f9be83658776cd4d9`  
		Last Modified: Mon, 11 Jul 2022 22:58:53 GMT  
		Size: 846.2 KB (846206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19491009819dbbd73e3c36f6e23d8e0dee2f2cd226bb85b6f8e75362ce2f2a8f`  
		Last Modified: Mon, 11 Jul 2022 22:58:53 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a99ccce4e746df3908e6d4145d6d73e77c4e66273cd843c76044b4dd0a9200a`  
		Last Modified: Mon, 11 Jul 2022 22:58:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20988dfe7bc351c0c048a38204c5d0cc44fe0733f460a3fe8735c2b8cc84feba`  
		Last Modified: Mon, 11 Jul 2022 22:58:53 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b6fc64822d213a76805d5fc94d9924f5510f57875cf14b30e2e59b73c37b10`  
		Last Modified: Mon, 11 Jul 2022 22:58:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
