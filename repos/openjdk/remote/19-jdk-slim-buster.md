## `openjdk:19-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:012dcdded6de1270ea7027edfb6add88a9edafaa4e408679a3e8293959c784dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:8bd3c35dc83db94c7a6302b6b5957befa2800e0e7f1ef145612c4d45d018926a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225459516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e76790fcdf830b813bcc94bb5f5268f948ee147fc332de95e33e5ad6907821`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:48:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 20 Apr 2022 10:48:29 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:48:29 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:21:36 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:21:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:21:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97724dec0639ffbe1d30e60defc8ff8fc2e27a3844e7c6173e64cb73e25b88`  
		Last Modified: Wed, 20 Apr 2022 11:02:57 GMT  
		Size: 3.3 MB (3273257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779cd26a6a36a4d1bf6f1a52a98791188144e2de18ea99cf42cdc58ad4617458`  
		Last Modified: Thu, 28 Apr 2022 23:30:58 GMT  
		Size: 195.0 MB (195045595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:98f71e3b22f81d441a6fda434a624e6748263514fc9fbd49460757d9c5a6fd9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222729357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fe05c13b58e3c6b00877e932b6b1df957eace201b00005005c8716ede63b06`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:25:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:25:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 20 Apr 2022 10:25:50 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:25:51 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:42:34 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:42:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:42:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4c0391a581a54e4ae08706ac3173bf39e99722f6efe3a9094dbe8916d7bfd`  
		Last Modified: Wed, 20 Apr 2022 10:47:49 GMT  
		Size: 3.1 MB (3125683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4506e886523b4b560ae2471ce8bace60d9fc4b9f9fa56695d0d14b04660fcb20`  
		Last Modified: Thu, 28 Apr 2022 23:58:36 GMT  
		Size: 193.7 MB (193695325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
