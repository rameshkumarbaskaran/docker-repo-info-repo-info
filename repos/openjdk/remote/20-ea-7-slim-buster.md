## `openjdk:20-ea-7-slim-buster`

```console
$ docker pull openjdk@sha256:7273de870f59e0ef690ef8bad90df0e036fd92bddd2d8eea30037f1e97125ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-7-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:c321aaafa45492afdb3a854501ddbd6fbb75a3f28e4b284346e9df086cec4f71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227836352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3053a5f38acde77c237fb09933fd0e2238d71cacfd0eabcd1ebb1f4f48881`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:56:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 12 Jul 2022 01:56:06 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:56:06 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:22:23 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:22:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:22:38 GMT
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
	-	`sha256:71b6c8ad454f53257a049d844f40aff5fadacc38a62410268bd272b5c4d7b673`  
		Last Modified: Thu, 21 Jul 2022 23:33:36 GMT  
		Size: 197.4 MB (197423073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b21ecb484d264b09528208257551096a6ee69d738c27ef0669528120b997dd40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225103194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707638a0eca747db5f8fd68adf50a2c233977f984b1bafe78fc2bbe593f04c25`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:29:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:29:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 12 Jul 2022 01:29:30 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:29:31 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:42:38 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:42:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:42:57 GMT
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
	-	`sha256:4c1076c68c6af81989c5350577b99105cc38b090e3bc1fed6961cbb1b54d539a`  
		Last Modified: Fri, 22 Jul 2022 00:01:56 GMT  
		Size: 196.1 MB (196062897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
