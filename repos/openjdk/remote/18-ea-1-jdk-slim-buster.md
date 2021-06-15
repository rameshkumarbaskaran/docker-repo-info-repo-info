## `openjdk:18-ea-1-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:122c1ba0a9fe52d9e62d0bd6570e5fb6d95e193f2d6bcfe42b592e223b6ee1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-1-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:501f719e6750075144bf7804f6aeb0d5dc5d7cb240f00bda1beb8434fcd2f491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218769638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb645c6b17a26e4c6aaff582b86e2553a7a43c98c1926bfedd8bbc20d8503e0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 14 Jun 2021 21:22:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Mon, 14 Jun 2021 21:22:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 21:22:29 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 21:22:29 GMT
ENV JAVA_VERSION=18-ea+1
# Mon, 14 Jun 2021 21:22:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='277c0021c542fbda35d2643351148fa6cceac66b5beca24016c75fafeed815de'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b615e986bc649e30072f1a7e88986e7a55cad95756c982a2f02f278ec8fe05c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:22:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b89b6081832b112f9483322d4710c661f12135e79279dc3fb1672883ada8d`  
		Last Modified: Wed, 12 May 2021 06:58:18 GMT  
		Size: 3.3 MB (3268772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a0aea412f7398eb9226f14e0336ca48f272a8934c12a40c5273a55c175675d`  
		Last Modified: Mon, 14 Jun 2021 21:30:33 GMT  
		Size: 188.4 MB (188354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-1-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a9a24656d245bb9a62347197ce602496cbf563df6cce1314c99c80937148d0da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216194656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d737cf735a674bde4a29708842462d388d91af0b1e7db87c3fe93502103aa1b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 May 2021 00:52:19 GMT
ADD file:91ba1791cab3ad29a1469d1e78f21f4c0b5d3d30598683b7104980604c318854 in / 
# Wed, 12 May 2021 00:52:34 GMT
CMD ["bash"]
# Thu, 27 May 2021 08:38:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 14 Jun 2021 20:43:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Mon, 14 Jun 2021 20:43:44 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 20:43:44 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 20:43:45 GMT
ENV JAVA_VERSION=18-ea+1
# Mon, 14 Jun 2021 20:43:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='277c0021c542fbda35d2643351148fa6cceac66b5beca24016c75fafeed815de'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b615e986bc649e30072f1a7e88986e7a55cad95756c982a2f02f278ec8fe05c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:43:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcad0c936ea5c12e1c8c4edb81a97c0cde04ee71e7067ee3b246474cf1854d7a`  
		Last Modified: Wed, 12 May 2021 01:02:02 GMT  
		Size: 25.9 MB (25911250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb067f13654098b66e57229fcd818a7d0f0c73bd34d158e3bedc28ee2a7b821`  
		Last Modified: Thu, 27 May 2021 08:54:42 GMT  
		Size: 3.1 MB (3118848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f449f31002bd588d868ece40bfdbca0ae927a497ec1f1c69dc25116d40075df`  
		Last Modified: Mon, 14 Jun 2021 20:58:22 GMT  
		Size: 187.2 MB (187164558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
