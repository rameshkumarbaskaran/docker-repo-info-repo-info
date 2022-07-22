## `openjdk:19-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:35ce1dbd4ba1d7880cfb72cc7a722bdcee588fae2cc34d4587da6a8444e94d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fe0e16bed06b36a9f73c293705d354367b7b8a5d539c297d71470c0a43500339
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229493452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb079e7789d4bfeff0f434b3ad8eea32cb41240a28cee4580f300b27eb472f62`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:57:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 12 Jul 2022 01:57:29 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:57:29 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:23:47 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:24:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:24:02 GMT
CMD ["jshell"]
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
	-	`sha256:6719c5c2d2f8549a98d068efb3fa8306df2baf9e7d97f889e7be4022d9674139`  
		Last Modified: Thu, 21 Jul 2022 23:36:05 GMT  
		Size: 196.5 MB (196544569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8ea4751a5addfba209f59478d8a49e8708e97d4b4a942a853a1f5705b6c08c8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226801646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c39bf539bfea70a64deb59804ea08ff0d06a767c27436d99b34e8d501832d9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:31:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 12 Jul 2022 01:31:05 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:31:06 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:44:18 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:44:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:44:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0eebdbddd0a55d86b14d45ff4aaee7c446d9188afe15e3a3295ef44d82e156`  
		Last Modified: Tue, 12 Jul 2022 01:49:35 GMT  
		Size: 1.6 MB (1565943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54f6cf03975c51a3ff3351898a1778a593180a07e056ee6ed1f8921525af8d0`  
		Last Modified: Fri, 22 Jul 2022 00:05:08 GMT  
		Size: 195.2 MB (195181477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
