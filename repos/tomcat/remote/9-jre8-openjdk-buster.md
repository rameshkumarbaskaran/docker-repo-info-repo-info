## `tomcat:9-jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:adb132b30fffd6cfe2819d465643bbe5eb4288eff5c1636abc73f6cbe5bac4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:db1b7d501d4108223ed254066a7fa37ec3e377982cb2e0cbadf3f0c8d96c1ada
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130080844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebcb85bd0e24a176e7dca20defac4a3edf1ab629cf8f50770dd8b1091bd3c3d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 01:20:26 GMT
ADD file:54d60144d251caa916ff50606bc2364131d47d6b10ed83d08c81c647ab56cc40 in / 
# Wed, 11 May 2022 01:20:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 05:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:53:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 11 May 2022 05:53:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 05:53:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:53:57 GMT
ENV JAVA_VERSION=8u332
# Wed, 11 May 2022 05:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 11 May 2022 23:56:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 May 2022 23:56:23 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 23:56:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 11 May 2022 23:56:23 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 May 2022 23:56:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:56:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 00:02:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 12 May 2022 00:02:24 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 May 2022 03:20:38 GMT
ENV TOMCAT_VERSION=9.0.63
# Wed, 18 May 2022 03:20:38 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Wed, 18 May 2022 03:20:38 GMT
COPY dir:495f7ec51315402274c7a73a36d9543fd27a76b8d010c62a3f1fc824e072dfdd in /usr/local/tomcat 
# Wed, 18 May 2022 03:20:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 03:20:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 18 May 2022 03:20:44 GMT
EXPOSE 8080
# Wed, 18 May 2022 03:20:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b03a94565ecb6e02edf716307f25a0ea5090e3e2f7acec6a3687b95415378a30`  
		Last Modified: Wed, 11 May 2022 01:25:33 GMT  
		Size: 50.4 MB (50437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7bcede80b1916d73be58ae0a2af8321770c4ce0c8ada05c39271e292355325`  
		Last Modified: Wed, 11 May 2022 01:58:28 GMT  
		Size: 7.9 MB (7856436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37471fc83c2dc382a8aec5dc1c1f0f2f8156f4df529cd1aea7647cbaee4b25fa`  
		Last Modified: Wed, 11 May 2022 01:58:28 GMT  
		Size: 10.0 MB (9997259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeeac3d88ceea1c7c59d0b4f6e44a633cd8d2c121c8d1955372d36690212534`  
		Last Modified: Wed, 11 May 2022 06:07:09 GMT  
		Size: 5.5 MB (5532625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5230153d4d0bf43116759b1e9d6c588d8825569f3ca615083095012d27f613`  
		Last Modified: Wed, 11 May 2022 06:10:11 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccae793566a93fcc6e4434b230e279258883952cb5de2fc06fdae2e1eebcb9a`  
		Last Modified: Wed, 11 May 2022 06:10:16 GMT  
		Size: 41.4 MB (41432105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ac4683eb2be26ef326a5842acb83f6221e6b3f11484f9c591266f81b5feafb`  
		Last Modified: Thu, 12 May 2022 00:25:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96930e3d1b89a319d729634746bfcafa490dc06e9a5c958da2b3cbfb8c8ef`  
		Last Modified: Wed, 18 May 2022 03:52:18 GMT  
		Size: 12.2 MB (12208511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7012e51912e8f182aae5548d9c7107e1e106e70489d05be4f8ee0ec198d11`  
		Last Modified: Wed, 18 May 2022 03:52:18 GMT  
		Size: 2.6 MB (2615430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad40672d0b19eb22bc4b2b4be6919f87bf1575717e56dce600f35d1bfe73e66f`  
		Last Modified: Wed, 18 May 2022 03:52:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:35ada82057718b754adb2278056ac6218c66186d97e389201aba4c81322526df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75da64095c19eabc1efb05d5fb0d05954ae008e1a18887debe462e0a05fa2e8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 00:47:11 GMT
ADD file:5389b77733b44ebc41850baff3ebfc491726af264a745f108d5f16076a0f04ab in / 
# Wed, 11 May 2022 00:47:11 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:26:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 14:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:25:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 11 May 2022 14:25:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 14:25:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:25:50 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 14:25:51 GMT
ENV JAVA_VERSION=8u332
# Wed, 11 May 2022 14:25:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 12 May 2022 03:17:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 12 May 2022 03:17:28 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 03:17:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 12 May 2022 03:17:30 GMT
WORKDIR /usr/local/tomcat
# Thu, 12 May 2022 03:17:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 03:17:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 03:26:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 12 May 2022 03:26:28 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 May 2022 02:45:00 GMT
ENV TOMCAT_VERSION=9.0.63
# Wed, 18 May 2022 02:45:01 GMT
ENV TOMCAT_SHA512=4b905018164026756bd36ab9fde8f6b21c886acb8e5255d93f8938491e4d375dd18b9fc58ee23e3d78b16e8b81271c1c998e5592beedcac632567c2ca9411c69
# Wed, 18 May 2022 02:45:03 GMT
COPY dir:b1d888cda186fdfdf26cffd817e05e04de23d61448bcad7809bddf951094f22e in /usr/local/tomcat 
# Wed, 18 May 2022 02:45:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 02:45:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 18 May 2022 02:45:09 GMT
EXPOSE 8080
# Wed, 18 May 2022 02:45:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5528d23e3f315103c99c14258e007a025d09bb4fd587c2d8a32d6dbb6047b891`  
		Last Modified: Wed, 11 May 2022 00:54:09 GMT  
		Size: 49.2 MB (49228300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b2d66a1dbe5960c6de4181ca3512467d3303dfb9cde3d92ecf7a85111cf68b`  
		Last Modified: Wed, 11 May 2022 01:37:01 GMT  
		Size: 7.7 MB (7719789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9244ac9f9851b43ddc1032930666d339c3a5d9b934e2ca42ecd2e8ef3dd680`  
		Last Modified: Wed, 11 May 2022 01:37:01 GMT  
		Size: 9.8 MB (9767329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc6f36efb47cf1dbb65f33c137b597dca68c3f097b894e7fa512565fdeebf8d`  
		Last Modified: Wed, 11 May 2022 14:44:32 GMT  
		Size: 5.5 MB (5506808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b49d458d1be38f46288de405c1c7c6640482e05bc6b9b0d6f4c99d541f8178`  
		Last Modified: Wed, 11 May 2022 14:48:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4977a3debfde6c21dba44b045b52f2480bf9d0fcf1717b77178023ced1e0c1e2`  
		Last Modified: Wed, 11 May 2022 14:48:10 GMT  
		Size: 40.7 MB (40672257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8e5ab66e9424ac92259ccd7dd09170db0b714de4e17d17e43ec6f8da3c84db`  
		Last Modified: Thu, 12 May 2022 04:02:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26a61a935cce3926d5b9dfcb2757bede5122cc38ecda21e9c7a13f1a34eb049`  
		Last Modified: Wed, 18 May 2022 03:30:40 GMT  
		Size: 12.2 MB (12224542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e727c90ef2504ac6239384baee7df9b667ae0a19bc673ad0e12508034a22c80`  
		Last Modified: Wed, 18 May 2022 03:30:38 GMT  
		Size: 2.3 MB (2285804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
