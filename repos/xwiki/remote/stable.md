## `xwiki:stable`

```console
$ docker pull xwiki@sha256:bf1c37dd4874a36d620841b52c69aec568387858925bf032f8262966d970deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:af3f0f850537d35635d2992e9eac5d8c8db78204fd7528f600757960ac1e2d76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.1 MB (631085811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791a3d6e7b206821884de01e8a29227b9cb5aec850d6704b6806aa7f6971e310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 19:38:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:38:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 19:38:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 19:38:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 19:38:32 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 19:38:33 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 19:38:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 21:45:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 21:45:47 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 21:45:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 21:45:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 21:45:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 21:45:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 21:54:48 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 28 May 2022 21:54:48 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 00:14:29 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 00:14:29 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 00:14:29 GMT
COPY dir:9e228650b85b87edd807ca8cfd0b3072b6311e9b245c8f24aeb48beb0c02b602 in /usr/local/tomcat 
# Fri, 10 Jun 2022 00:14:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 00:14:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 00:14:34 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 00:14:34 GMT
CMD ["catalina.sh" "run"]
# Fri, 10 Jun 2022 05:08:30 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 10 Jun 2022 05:08:30 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 10 Jun 2022 05:08:30 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 10 Jun 2022 05:08:30 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 10 Jun 2022 05:08:30 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 10 Jun 2022 05:08:31 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 10 Jun 2022 05:09:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 05:09:11 GMT
ENV XWIKI_VERSION=14.4.1
# Fri, 10 Jun 2022 05:09:11 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Fri, 10 Jun 2022 05:09:11 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Fri, 10 Jun 2022 05:09:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 10 Jun 2022 05:09:49 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 10 Jun 2022 05:09:49 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 10 Jun 2022 05:09:49 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 10 Jun 2022 05:09:49 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 10 Jun 2022 05:09:49 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 10 Jun 2022 05:09:50 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 10 Jun 2022 05:09:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 10 Jun 2022 05:09:50 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 10 Jun 2022 05:09:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 10 Jun 2022 05:09:51 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Jun 2022 05:09:51 GMT
VOLUME [/usr/local/xwiki]
# Fri, 10 Jun 2022 05:09:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 05:09:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b879d05afe7d1ed6ac0f5b2d9537450b8058210d5c1ba04e3dbdfd0ea7f44da0`  
		Last Modified: Sat, 28 May 2022 19:48:32 GMT  
		Size: 5.7 MB (5657595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67409f01891c54bb4d7cf58512ec5cef2762ae616c2ab81d132c671c585f27b4`  
		Last Modified: Sat, 28 May 2022 19:48:31 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777f3575eb5979e51c7805e2bf9b825868bbd06f981240a48991e55828c1f206`  
		Last Modified: Sat, 28 May 2022 19:48:38 GMT  
		Size: 47.2 MB (47197487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b03265e3e87ebc901b1160b3b4f25f1e477105358369d25546a30af93d003c`  
		Last Modified: Sat, 28 May 2022 22:14:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e566ee03dd6511e1cf3dbf942b1ecd40cb8c4a96c04fb6abf3c6ae3aa07e8fe2`  
		Last Modified: Fri, 10 Jun 2022 00:38:05 GMT  
		Size: 12.2 MB (12157771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f140bf5d88f3a093cb01bb4263c2cbc0df56696ccb6c5095209c5ece7bc4e6d`  
		Last Modified: Fri, 10 Jun 2022 00:38:04 GMT  
		Size: 459.7 KB (459743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb8433c374cdbc7ca8cb7e41d963bf9173063ae0e2b5ac3d17af704e4e9e2b3`  
		Last Modified: Fri, 10 Jun 2022 00:38:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe3b54404fe94aff8afeff09b1f8b973b22fca941c23295fdddcfc9a888ee8`  
		Last Modified: Fri, 10 Jun 2022 05:14:17 GMT  
		Size: 200.2 MB (200196667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3d2e0c5e558a54ce22e7edb6fab172c9888326c7e0753d0509d909ffeaff50`  
		Last Modified: Fri, 10 Jun 2022 05:14:05 GMT  
		Size: 292.0 MB (291982552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06091595657fcd37ac7fcc2411c92a171d07a73da6cea94ca8b8cc492fc691eb`  
		Last Modified: Fri, 10 Jun 2022 05:13:47 GMT  
		Size: 2.4 MB (2381179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bc17be8f637f238539c9cb6c26c3c0e7868d697b979734dd1dfb66c58afe5`  
		Last Modified: Fri, 10 Jun 2022 05:13:47 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e793032d13fbfc8fc6bc0f0eb1efa04ae16e2a7172c415b17db9fc8c9383c8`  
		Last Modified: Fri, 10 Jun 2022 05:13:47 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934625d926bea7412216e6271b6aa10295ca3fd73fff24c56811929315e69fe7`  
		Last Modified: Fri, 10 Jun 2022 05:13:47 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d821076b73a0c1dfe39a3a71ab21fa093ae6b1ba1fb465904ab8f79894bef0`  
		Last Modified: Fri, 10 Jun 2022 05:13:47 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c587888b4c64640c08c2d6160ee9bf5f66ceebaa3ef3fc07599d0073c472887f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.4 MB (623443572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36aeb125a5fbddd49e054f92cbbb930bb157fb56956acdd79e063b35a69d4c0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 16:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:50:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 16:50:25 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 16:50:26 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 16:50:27 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 16:50:28 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 16:50:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 20:03:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:03:46 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:03:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:03:48 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:03:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:03:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:19:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 28 May 2022 20:19:41 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:23:48 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:23:49 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:23:51 GMT
COPY dir:8b2659fab371903313049a2ccb14f476997d306283d017886678e55926297afe in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:23:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:23:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:23:56 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:23:57 GMT
CMD ["catalina.sh" "run"]
# Fri, 10 Jun 2022 07:40:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 10 Jun 2022 07:40:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 10 Jun 2022 07:40:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 10 Jun 2022 07:40:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 10 Jun 2022 07:40:27 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 10 Jun 2022 07:40:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 10 Jun 2022 07:41:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 07:41:01 GMT
ENV XWIKI_VERSION=14.4.1
# Fri, 10 Jun 2022 07:41:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.4.1
# Fri, 10 Jun 2022 07:41:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=8e20eba50acee0f157d3cc160306d65e0995b453833c8923f833030f0a469fb4
# Fri, 10 Jun 2022 07:41:43 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 10 Jun 2022 07:41:44 GMT
ENV MYSQL_JDBC_VERSION=8.0.29
# Fri, 10 Jun 2022 07:41:45 GMT
ENV MYSQL_JDBC_SHA256=d4e32d2a6026b5acc00300b73a86c28fb92681ae9629b21048ee67014c911db6
# Fri, 10 Jun 2022 07:41:46 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.29
# Fri, 10 Jun 2022 07:41:46 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.29.jar
# Fri, 10 Jun 2022 07:41:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.29.jar
# Fri, 10 Jun 2022 07:41:49 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Fri, 10 Jun 2022 07:41:50 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 10 Jun 2022 07:41:51 GMT
COPY file:1b8409986f3e4eb79a7a0b18472cb2692a61d504fb5ef34292bc997b79fd760d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 10 Jun 2022 07:41:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 10 Jun 2022 07:41:53 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Jun 2022 07:41:54 GMT
VOLUME [/usr/local/xwiki]
# Fri, 10 Jun 2022 07:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 07:41:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62ee63325dbbad699d6845f68c2391db3bf158f60373849c2d1cb6bb479788`  
		Last Modified: Sat, 28 May 2022 11:17:05 GMT  
		Size: 4.9 MB (4938744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e37b4c58dd1db7ead6f3c2cdf757f490b4e29c958d2a70559c313e9a03a5ef`  
		Last Modified: Sat, 28 May 2022 11:17:06 GMT  
		Size: 10.7 MB (10657073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29312e2f0b2d2423a19b1e65da0020d22da272698007d994eb022cafc68c98dc`  
		Last Modified: Sat, 28 May 2022 17:06:29 GMT  
		Size: 5.6 MB (5649779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89bea478de23120f9e854c805b853218e7d1c2b55ab2f0d9fa8a312c41bf12`  
		Last Modified: Sat, 28 May 2022 17:06:29 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ea084fee99e1a8783492e9519624f9d393b283f712e81f1af19c68ce1ce2a`  
		Last Modified: Sat, 28 May 2022 17:06:36 GMT  
		Size: 46.5 MB (46498872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d4a73df71717612d4f66dd4836687d3d09cf2d630603fdd04ec76af94b297`  
		Last Modified: Sat, 28 May 2022 20:53:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08687feb72b7bf15bb5066246ace6f0ad06423c95c7338b07ab121e7128b74bb`  
		Last Modified: Fri, 10 Jun 2022 02:00:00 GMT  
		Size: 12.2 MB (12167371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb8c7ae36a9e5aa1fc15fbb39d56104d79d9e2db26dda9a679989a3c41c274b`  
		Last Modified: Fri, 10 Jun 2022 01:59:59 GMT  
		Size: 217.2 KB (217175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c96679f6c47929abc561a747f094e1d41c3ce1ede6bce67f28240c3b67de0`  
		Last Modified: Fri, 10 Jun 2022 07:47:47 GMT  
		Size: 195.2 MB (195241607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca845dbef720edc7efd6f950094cbfeaca75450c61ac6255bcf0374054b5542`  
		Last Modified: Fri, 10 Jun 2022 07:47:42 GMT  
		Size: 292.0 MB (291982469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617bd79920c9fdb565692846bb165e0ffdcbf856b9488d47e60f9d83cc59e610`  
		Last Modified: Fri, 10 Jun 2022 07:47:20 GMT  
		Size: 2.4 MB (2381173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2d513c50299cd29563fe8b8083f9ab344caf95f21762fa4bb2846dc475b091`  
		Last Modified: Fri, 10 Jun 2022 07:47:20 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fc43efa23f5571065521f66fef7ebd5ab71b123b22ff2a26a6c56fc7ff4bb6`  
		Last Modified: Fri, 10 Jun 2022 07:47:20 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c7cd6a1cb2e7658583f5f4dc1be5f4e429bf1e53e565e52fbfd222238a134d`  
		Last Modified: Fri, 10 Jun 2022 07:47:20 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4892210cf94b1df6ab567d8a954fc097f09b2069961a6edbce2a1edfde07a87a`  
		Last Modified: Fri, 10 Jun 2022 07:47:20 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
