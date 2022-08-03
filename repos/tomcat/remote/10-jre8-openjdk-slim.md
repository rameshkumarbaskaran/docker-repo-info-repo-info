## `tomcat:10-jre8-openjdk-slim`

```console
$ docker pull tomcat@sha256:b395b14aea31a4e722270c4834e878d286444ae13149e795cb03cc21760a96bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre8-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:c89ac9aff5d8b35a224ae8bcdf977f6bae9bc5936edb6e2e9dd1f646a78f8991
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87583788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0d05b0d02d02aa0114b41188090659d1e39461b9ee0b802c53353608a491e3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:29:45 GMT
ENV JAVA_VERSION=8u342
# Mon, 25 Jul 2022 20:30:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_8u342b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_8u342b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Mon, 25 Jul 2022 23:14:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 23:14:25 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 23:14:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 23:14:26 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 23:14:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:14:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:14:26 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 25 Jul 2022 23:14:27 GMT
ENV TOMCAT_MAJOR=10
# Wed, 27 Jul 2022 01:37:30 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 27 Jul 2022 01:37:30 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 27 Jul 2022 01:37:30 GMT
COPY dir:45b0c29c97a7833805c233da0509a5932d4c29db5d24cf46a7e5bb66aae881d9 in /usr/local/tomcat 
# Wed, 27 Jul 2022 01:37:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 01:37:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Jul 2022 01:37:36 GMT
EXPOSE 8080
# Wed, 27 Jul 2022 01:37:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c195552e7f0d9051e292aab20f5a012de83951109edb0fcb133afd5af9cdb5b`  
		Last Modified: Mon, 25 Jul 2022 20:49:34 GMT  
		Size: 41.7 MB (41696209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014ae659d4df1633b279981d5c5a577c22777056b35247525ac0d0edd82f305d`  
		Last Modified: Mon, 25 Jul 2022 23:42:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d8926f9899544ea31d5b2fec1c2cbb8099155615268f63a171bd6d3f613316`  
		Last Modified: Wed, 27 Jul 2022 02:04:00 GMT  
		Size: 12.5 MB (12541882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d565e1fb0dffa4b5648d6b30f170fe95a9c19b151f5f45cb9b531dfd7749864`  
		Last Modified: Wed, 27 Jul 2022 02:03:59 GMT  
		Size: 396.3 KB (396300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b372880888a9ab12b2ed95314b80974602666a68efa06e353b4972e97227687e`  
		Last Modified: Wed, 27 Jul 2022 02:03:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre8-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1996f23880de37883e2cb42616d2bc74b74ca97928755b0a5ff46affab756e35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85086090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1154da22fc94d50632e940e6a7d273223bf93f3c12f917f1810f4caee9972464`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:51:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 02 Aug 2022 04:52:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 02 Aug 2022 04:52:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:52:02 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 04:52:03 GMT
ENV JAVA_VERSION=8u342
# Tue, 02 Aug 2022 04:53:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_8u342b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_8u342b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 03 Aug 2022 02:03:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 02:03:06 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 02:03:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 02:03:08 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 02:03:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:03:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:03:11 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 03 Aug 2022 02:03:12 GMT
ENV TOMCAT_MAJOR=10
# Wed, 03 Aug 2022 02:03:13 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 03 Aug 2022 02:03:14 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 03 Aug 2022 02:03:16 GMT
COPY dir:a762b5030df1295b3eb1eb72ea19c8b258a69287b1bb14a3ebffdf20fe793418 in /usr/local/tomcat 
# Wed, 03 Aug 2022 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 02:03:21 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 02:03:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4015b6e8cc8db11af172df5c0369552bc2a74cd69094b0756d21fc6b0b2a5393`  
		Last Modified: Tue, 02 Aug 2022 05:03:25 GMT  
		Size: 1.6 MB (1565954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86b181efa02db2dd92e3f621ee71d8ddebe2669b3dba8a0320d1d9419b1c7a`  
		Last Modified: Tue, 02 Aug 2022 05:18:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94abd992e68d552cfc81a28ad6e8a9000e08769135a27bad79a59d05044bd63b`  
		Last Modified: Tue, 02 Aug 2022 05:20:31 GMT  
		Size: 40.7 MB (40732494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37315976878163c22f5f880c2fd3a959c2d52498a094aec357dd1d976c70bc15`  
		Last Modified: Wed, 03 Aug 2022 03:09:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daceef10e09c520519c4df4260788ea14081fbcf15b0346155038938c8a0b3a`  
		Last Modified: Wed, 03 Aug 2022 03:09:59 GMT  
		Size: 12.6 MB (12553099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1781029360c04c481d3a147b9756a124fc55f39b1b8f2d53d96ddbccaaaf82d0`  
		Last Modified: Wed, 03 Aug 2022 03:09:57 GMT  
		Size: 179.9 KB (179888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
