## `openjdk:19-slim-buster`

```console
$ docker pull openjdk@sha256:af33033209691481983d2eadb2a289600db4428fad13da897d186762cc5bd34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:d501bf1ddfa55a1c6788a423d7639699976ad019f1cebc442d45debe17207340
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226959221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e354d60e3eacd3c6473f6aac0c5dee657190d0ca4c2da3e205ac29194ad995fc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:58:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 12 Jul 2022 01:58:02 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:58:03 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:24:21 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:24:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:24:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62264f680cd73ea710b719ee1e279e0a800def0defab33dd092436647625fa1a`  
		Last Modified: Tue, 12 Jul 2022 02:10:29 GMT  
		Size: 3.3 MB (3273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51d1109e10c6eed59c33ba73a9a177953a3f5075b628eeb1c6f3ffb39360ca`  
		Last Modified: Thu, 21 Jul 2022 23:37:27 GMT  
		Size: 196.5 MB (196545942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ba075ba7950b01d1976247fffd92c4e1f09fd2813b32da791da4eb22a1532ff1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224227906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e40cc8db957b574d8d86b930ea2babcdd2b2e7db2940abe49e4328568aba921`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:29:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:31:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 12 Jul 2022 01:31:54 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:31:55 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:45:06 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:45:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:45:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebd82c0fcc991163b8dd04e396a3c7388adb7b021c0463cecaa0345cbd7ac1b`  
		Last Modified: Tue, 12 Jul 2022 01:51:21 GMT  
		Size: 3.1 MB (3126061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56c69a8686bcf320141eab55ed20cbeff46a58960eb5cc56f17f122cf1117d8`  
		Last Modified: Fri, 22 Jul 2022 00:06:51 GMT  
		Size: 195.2 MB (195187609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
