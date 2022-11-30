## `openjdk:20-buster`

```console
$ docker pull openjdk@sha256:b8faf13293e7f3d8ddafacadfb87396be19c6d9409d11de5f2ab2c905aaf8288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:700529c4bb2d1abfe5657b5dd8ee191ebd2e354fbfbed13784b4f45fbe83cf3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332152334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8490818d255de4f9049c4ac5eb6ec9fa62a24dc178cba33087d1f87d881fb2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:25:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:25:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 10:25:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:37:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:37:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 13:37:41 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:37:41 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 21:31:29 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:31:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 21:31:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a122751b35336c158fc53a3bb03c6b11b414387589e5455e99baecdd803c6318`  
		Last Modified: Tue, 15 Nov 2022 10:32:48 GMT  
		Size: 7.9 MB (7858972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a277c3efe7c0d28e443180df5a70570f6baed1f16a4ceeb88e9dd299df62dc6`  
		Last Modified: Tue, 15 Nov 2022 10:32:48 GMT  
		Size: 10.0 MB (10001396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c35b81c50326813f61c6bd62a84551d9bac477bfc60a617c692b7d12d306f1`  
		Last Modified: Tue, 15 Nov 2022 10:33:04 GMT  
		Size: 51.8 MB (51843950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7dd149c29a78af7c20ad717829dd1cdfb609af8e9f186fb42828829c4d0694`  
		Last Modified: Tue, 15 Nov 2022 13:42:53 GMT  
		Size: 13.9 MB (13927479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73269394bc6ea89ebdf0e960610769221a25bb89a05f8bf0f37bee9d9661a125`  
		Last Modified: Wed, 30 Nov 2022 21:37:02 GMT  
		Size: 198.1 MB (198071714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ad4d0c040a9dbe314794c9aa78d35a75d578636592eb22bcf5eb5bda0ba63a84
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330416891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335a7226d803642d9f64119ea61dee710e0ed2228ea4afa2acde4cf5d8a176a8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:37:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:38:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:59:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 06:59:46 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 06:59:46 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 20:55:26 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 20:55:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 20:55:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35873fa6ec375a28180771e63a96f2039703f6658efa32da2e83a64f6919bf1e`  
		Last Modified: Tue, 15 Nov 2022 05:43:54 GMT  
		Size: 7.7 MB (7726432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07615c620859a5288e844fd58e708c735c884a4b600e9ea4bd3f26ca5744f723`  
		Last Modified: Tue, 15 Nov 2022 05:43:55 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02969cbb07458e1786c56d183fed53adf7ef70ff25d0fc5541b85e728573ba7`  
		Last Modified: Tue, 15 Nov 2022 05:44:10 GMT  
		Size: 52.2 MB (52172432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f64415bb9e10e81c79af9306768e42eb71ed0934752a69a80f1de65db0608`  
		Last Modified: Tue, 15 Nov 2022 07:05:07 GMT  
		Size: 14.7 MB (14672752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f54db5425a2e5b24f64b3c1a7e0d5f74f6bb706553713ecdf5c50f11b6584e`  
		Last Modified: Wed, 30 Nov 2022 21:01:16 GMT  
		Size: 196.6 MB (196607908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
