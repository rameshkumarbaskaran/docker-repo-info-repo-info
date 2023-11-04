## `openjdk:22-slim-bullseye`

```console
$ docker pull openjdk@sha256:7ded38224fef104d933850bb17c19d5b8411aaeaabf97e5c3c385e80da471ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:64f5e2dceee2157867f832cbf3330af591112d9e3c28368f29f841def44089de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239151621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8760719ff14d76a16c0256228be2fdee466c3baafaf04610043e4c6558e997`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:51:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 11:51:40 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 11:51:40 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2023 00:56:43 GMT
ENV JAVA_VERSION=22-ea+22
# Sat, 04 Nov 2023 00:57:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/22/GPL/openjdk-22-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='d6c2ae7f19a6ac9f7621d63fd978e6858b099a707b7d3e2a709cd18ebb0b9f61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/22/GPL/openjdk-22-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='8ab5ab05cfca072f17b60158a4fb90db6e34a08bc815348729d0965e6bdf983a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Nov 2023 00:57:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8bcc04d7ec7c559e1809ac80f8625104e0723f3b628adcb9e7dd5ead853567`  
		Last Modified: Wed, 01 Nov 2023 11:54:41 GMT  
		Size: 1.6 MB (1584394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad23e68a6d5a178386d4fac0b06f2a0e4ec490e23c8d5c5443135ce4a4067df`  
		Last Modified: Sat, 04 Nov 2023 01:01:10 GMT  
		Size: 206.1 MB (206149312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d0b74000bd20aed3a4765d9f7601ee8c2f9ad2b960def90d6dfb5f6b8ecb4ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235943050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1b710bca15abef909c53dd08ff15246da3301e6274dac4f5c4ae4390e3673d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 03:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:22:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 03:22:54 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:22:54 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2023 00:43:06 GMT
ENV JAVA_VERSION=22-ea+22
# Sat, 04 Nov 2023 00:43:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/22/GPL/openjdk-22-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='d6c2ae7f19a6ac9f7621d63fd978e6858b099a707b7d3e2a709cd18ebb0b9f61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/22/GPL/openjdk-22-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='8ab5ab05cfca072f17b60158a4fb90db6e34a08bc815348729d0965e6bdf983a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Nov 2023 00:43:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c6abed9fe365e0d3d29c1e8623c6d3d6cc0edf4c4d111f36535cad5d6bfe0c`  
		Last Modified: Wed, 01 Nov 2023 03:25:23 GMT  
		Size: 1.6 MB (1567882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d19411ce2c81e9e8cbb8bc36f518c97c9a481d5439a58fb60ad4f87fb64d1b`  
		Last Modified: Sat, 04 Nov 2023 00:47:13 GMT  
		Size: 204.3 MB (204311263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
