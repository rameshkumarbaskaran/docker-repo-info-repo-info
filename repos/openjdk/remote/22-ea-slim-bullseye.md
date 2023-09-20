## `openjdk:22-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:f0c781eb696cfdfc568d425e12cea69985b14c7b6f25a552c058e3eb345ee7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:164b4bd296d66e1ba4de705016b1ad91ca4a32f782d946f66b7b2d9645e80410
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238453902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4009d9056f856b7c862c3f1f121042812d14d741c3bf6c44b151c8bba2ed13ea`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:16:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 06:16:45 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:16:45 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 06:16:45 GMT
ENV JAVA_VERSION=22-ea+15
# Wed, 20 Sep 2023 06:16:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Sep 2023 06:17:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6450b6ea4fa89bead82ea896a53e3dfc6ad66d97a14a9f56241d71c097c8e0e1`  
		Last Modified: Wed, 20 Sep 2023 06:19:33 GMT  
		Size: 1.6 MB (1582466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60f9dc3d3af6222f8c43f0bcd4b845230bc6ac46965a59a886f904257c03e0a`  
		Last Modified: Wed, 20 Sep 2023 06:19:47 GMT  
		Size: 205.5 MB (205453725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fa7de317fa503b6645157db51f8d20a7845acdc302b6f2bf42df56cde247e2ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235397844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c82747c9b1d6c232f42b6c4cbf86950447f95bfe9bfba3a7e166ecdddfb668`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:58:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:58:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:58:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:58:12 GMT
ENV JAVA_VERSION=22-ea+15
# Wed, 20 Sep 2023 17:58:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Sep 2023 17:58:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cb87782f1498c5adbce22d6724eb58d2770ffdc0c184aa7d27ca35e61138f`  
		Last Modified: Wed, 20 Sep 2023 18:02:07 GMT  
		Size: 1.6 MB (1566445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdad06ef83130b545bf801fac2ca6cc1371374a9632c38bd6de2de0cb6244efc`  
		Last Modified: Wed, 20 Sep 2023 18:02:19 GMT  
		Size: 203.8 MB (203768530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
