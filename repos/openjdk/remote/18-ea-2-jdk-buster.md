## `openjdk:18-ea-2-jdk-buster`

```console
$ docker pull openjdk@sha256:604e32f608bdd6f679e1dbb00fad8da616f9de79c5d87af9df6bfdce9aafa475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-2-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:5394bceb5e0d0ca1d0d7ac234b216513bb8e4f87bf83866198383aed075e0b41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322156320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abbf9e024600c7104577fdc45287375d184c3144b5d7af78f1a00cf7194695f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 14 Jun 2021 21:22:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Mon, 14 Jun 2021 21:22:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 21:22:13 GMT
ENV LANG=C.UTF-8
# Tue, 22 Jun 2021 21:39:12 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:39:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:39:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53c8574903f2e47274cfe45903823235a9b4b846f7771f2a75a8e6a1462162`  
		Last Modified: Wed, 12 May 2021 06:57:35 GMT  
		Size: 13.9 MB (13921268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3464d7e2ec4eb8e5a7b43cac355aa9cdd6965aeadebb7dc4b8ac8bbfa8d1454`  
		Last Modified: Tue, 22 Jun 2021 21:47:45 GMT  
		Size: 188.1 MB (188130247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-2-jdk-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c65fb25ee62c18bcd147d465671b6693d6987b6c3a3e1576a5a52a2ac019d279
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320684913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9462dcadea7e605591ac8531ddba58140144f883e82f5364dad06d567ef7517d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 20:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 14 Jun 2021 20:43:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Mon, 14 Jun 2021 20:43:27 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 20:43:27 GMT
ENV LANG=C.UTF-8
# Tue, 22 Jun 2021 21:57:30 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:57:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:57:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8aff564b222789ed2823b88e0f1a69ac00cbcbf9349acb8a363d5ef9724182`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e893e0778bb86166fb6799aec4e4ac337c4f10172386c8ae9cf3c787331d7d`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 10.0 MB (9984325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf2dd6193dae84aecaec1d65081288ca49fe0843460035cc060b5aa4e7a9a7`  
		Last Modified: Thu, 27 May 2021 21:05:39 GMT  
		Size: 52.2 MB (52167766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e4f34f8162390a1c3755bde6c4b80914f4d5f6e0b090336929fcc052d69dd1`  
		Last Modified: Fri, 28 May 2021 05:32:23 GMT  
		Size: 14.7 MB (14673533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b8dfb0e6967c5e803b949f7b41a4d6397f20a981c9d852231ffb0282497a94`  
		Last Modified: Tue, 22 Jun 2021 22:12:04 GMT  
		Size: 186.9 MB (186939032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
