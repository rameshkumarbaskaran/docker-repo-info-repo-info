## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:cf31a99df6d278bae035b083736559009bb014965e15ce4bff5a910000875d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:a13301bbe530934422bf1545a1574ca9c55d8daff0b061aaaba35ad304300afd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.6 MB (639592842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635b94376eaa5b95c7f3430b118cd65ce1a1b04547fa0b4b70c3b7fcf0ec3dd0`
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
# Wed, 13 Jul 2022 07:17:37 GMT
ENV XWIKI_VERSION=14.5
# Wed, 13 Jul 2022 07:17:37 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.5
# Wed, 13 Jul 2022 07:17:37 GMT
ENV XWIKI_DOWNLOAD_SHA256=fdf6397ebb0036920953d5e7f6d3896b3b8744517b8f00822c31380c24a3e170
# Wed, 13 Jul 2022 07:18:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 13 Jul 2022 07:18:19 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 13 Jul 2022 07:18:20 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 13 Jul 2022 07:18:20 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 13 Jul 2022 07:18:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 13 Jul 2022 07:18:20 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 13 Jul 2022 07:18:20 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 Jul 2022 07:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Jul 2022 07:18:21 GMT
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
	-	`sha256:743e40d0e23728a9aa67b9297ef782c286a89218321bfb3f00bd83632df94c41`  
		Last Modified: Wed, 13 Jul 2022 07:22:36 GMT  
		Size: 301.2 MB (301166445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564325e6e912f8d3704717609cdce23b0ccfb9b0d2457bc6b6da3656e96457d9`  
		Last Modified: Wed, 13 Jul 2022 07:22:17 GMT  
		Size: 846.2 KB (846208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae44387a65ed38c803cd9560890188559f4021a73d039a92be597def15dc6c`  
		Last Modified: Wed, 13 Jul 2022 07:22:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddcdf3bcf9e410ac638066d88686c088d4abc38dabfbc2e9f6b4d8f001eaf61`  
		Last Modified: Wed, 13 Jul 2022 07:22:16 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a3d3350cd84ca366fe2664dc55b6d0500e88640fafcc55a2a851e6a61029c0`  
		Last Modified: Wed, 13 Jul 2022 07:22:16 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2711d5d0038ef6229f6fc880e68fdc9c6106803ebd19fc4ba43530892240b281`  
		Last Modified: Wed, 13 Jul 2022 07:22:16 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8f96915ca73ffa1faa241268096bc8a618426a9c735fbc736a963e491c1cc0bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.9 MB (631947925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d420b2561d3f000b09ca2774ac06101ae9d166b2ba241de4df41aa427423b`
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
# Mon, 11 Jul 2022 22:49:43 GMT
ENV XWIKI_VERSION=14.5
# Mon, 11 Jul 2022 22:49:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.5
# Mon, 11 Jul 2022 22:49:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=fdf6397ebb0036920953d5e7f6d3896b3b8744517b8f00822c31380c24a3e170
# Mon, 11 Jul 2022 22:50:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Mon, 11 Jul 2022 22:50:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Mon, 11 Jul 2022 22:50:25 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Mon, 11 Jul 2022 22:50:26 GMT
COPY file:4a923f484bb29a26630c19e1d617d3bf6aa6ae7c6c4a5561e97b037bcde0847c in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Mon, 11 Jul 2022 22:50:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Mon, 11 Jul 2022 22:50:28 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 11 Jul 2022 22:50:29 GMT
VOLUME [/usr/local/xwiki]
# Mon, 11 Jul 2022 22:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Jul 2022 22:50:30 GMT
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
	-	`sha256:20e72e0299f1b79124d33bd1271c26cd2c910e6b7175acb67951b05c26d15366`  
		Last Modified: Mon, 11 Jul 2022 22:56:45 GMT  
		Size: 301.2 MB (301166387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93d39ea38f183395408ec3fdc3138ec94ca615664dc2ec220b498047969cd7`  
		Last Modified: Mon, 11 Jul 2022 22:56:23 GMT  
		Size: 846.2 KB (846208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980080b1ffd55e321b79bf36f4a6e9e79c7323f7e17c7702b3779a1b9b60c5b6`  
		Last Modified: Mon, 11 Jul 2022 22:56:22 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf72a86d8c0be4bee89f45ac128e71c58cab6ca41ce8e268973b490d16ec30b`  
		Last Modified: Mon, 11 Jul 2022 22:56:22 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ea3d5bca79099801a96b70c21d2970440cce02fc7cf1d44f74b99fdc68049d`  
		Last Modified: Mon, 11 Jul 2022 22:56:22 GMT  
		Size: 5.9 KB (5870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67763da40efe273c82889b9b1205b572870cbb13e5267a86381c965d3ebb629`  
		Last Modified: Mon, 11 Jul 2022 22:56:22 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
