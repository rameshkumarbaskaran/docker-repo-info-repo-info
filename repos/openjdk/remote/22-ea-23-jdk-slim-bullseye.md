## `openjdk:22-ea-23-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:32dcd71705a0e74b3b83d93294afb70c6eb57cf694ccb8dd558724d744bc098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-23-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7d265f186b8a716902d1d3a3388a8e9c24c31c5cf9afe6b31e8d33ae7a554bc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238507173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c399d25169ea3d2cd8cd4aa4b29712bc11a275b0c70b3549bbbae7df7e5729`
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
# Wed, 15 Nov 2023 05:29:05 GMT
ENV JAVA_VERSION=22-ea+23
# Wed, 15 Nov 2023 05:29:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='fd781d8f07801adbe2c55425b595cf97d4652de7f27a56d90a5daabd8d899a22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5480254852c4d9b56987eab704922c5174895ef4b11407a0e79c887bf89ffe24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 15 Nov 2023 05:29:22 GMT
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
	-	`sha256:42b05b06b26838bc9711ad94e4a8b53b9e542bb62a7aa83d872b84fbafc7ac63`  
		Last Modified: Wed, 15 Nov 2023 05:33:22 GMT  
		Size: 205.5 MB (205504864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-23-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:68d186f13e3f880c814055aa6901119c8ec9c6f7b8e6753773f7a6052987e3d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235350362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d3274cc71156736cb5eed8cfc41871017562244bc7bc569bd90417cb08392a`
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
# Wed, 15 Nov 2023 01:56:37 GMT
ENV JAVA_VERSION=22-ea+23
# Wed, 15 Nov 2023 01:57:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='fd781d8f07801adbe2c55425b595cf97d4652de7f27a56d90a5daabd8d899a22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5480254852c4d9b56987eab704922c5174895ef4b11407a0e79c887bf89ffe24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 15 Nov 2023 01:57:06 GMT
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
	-	`sha256:476ab37758c98083770eb16438a3ebfce9b5f5f6272203f2cf9509e7ffd79a5c`  
		Last Modified: Wed, 15 Nov 2023 02:00:54 GMT  
		Size: 203.7 MB (203718575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
