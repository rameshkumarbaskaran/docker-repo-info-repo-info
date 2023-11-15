## `openjdk:22-ea-23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:e09fc2413a6c9fee00c25af7f80269fc08d3f7f40b3218102e231130761af4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2ff5a8fbde8e072e81d54749ad75a64b0218e6d7f2d7dfef6ec1ca9b038c43c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358379499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bcd18188cb7377fbd3d798c1ab3fd2874e879e9cd9b5251f5ba1082b086ef1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:04:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:21:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 03:21:48 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Nov 2023 01:54:57 GMT
ENV JAVA_VERSION=22-ea+23
# Wed, 15 Nov 2023 01:55:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='fd781d8f07801adbe2c55425b595cf97d4652de7f27a56d90a5daabd8d899a22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5480254852c4d9b56987eab704922c5174895ef4b11407a0e79c887bf89ffe24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 15 Nov 2023 01:55:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198068495d09b6865e75ce28d5d5d5de39897b8325ada63ba80eca884ad5666b`  
		Last Modified: Wed, 01 Nov 2023 02:13:57 GMT  
		Size: 64.0 MB (63994018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459caeca6f2dabcdd676f48943e8a6f36c3bf3fb165acf2bdab551ecf3414f6`  
		Last Modified: Wed, 01 Nov 2023 03:23:46 GMT  
		Size: 17.7 MB (17733531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f424ee6959d2b093897f08818a30530ec24e97d5c24fea3f785eb285422b2cb7`  
		Last Modified: Wed, 15 Nov 2023 01:59:05 GMT  
		Size: 203.5 MB (203454401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
