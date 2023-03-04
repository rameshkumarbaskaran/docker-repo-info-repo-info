## `openjdk:21-ea-12-slim-bullseye`

```console
$ docker pull openjdk@sha256:6ddeadea0dce50582525e466d19a884b9447ba22cf26374e6271bf99423f2ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-12-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a933c2d39dc2913740236f69a212ca367b06cf9d1c50016a6b1898f306a81f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232783486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f32761b11f867f6827c279e4925f1ba1547c8157bc10d0d11d7c7263c0d9e64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:42:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:42:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 08:42:26 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 08:42:26 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:27:16 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:27:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:27:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c16718086ec84986f6c86486062a7b0076aa837de91233c7c3405f3e6bcb01`  
		Last Modified: Wed, 01 Mar 2023 08:46:37 GMT  
		Size: 1.6 MB (1582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02994a73498939405716c73ef3e58ff122fabed3853c7269fc9961cad322aa0`  
		Last Modified: Sat, 04 Mar 2023 00:31:41 GMT  
		Size: 199.8 MB (199789776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-12-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:03bc2961a80cfc76061bd3dae13587d159b7be0d1a93f029bb1a74f931c41213
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229903261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023592737223e96cf46a5b2705356426f9bc69e3990ef6512ce6d972689972c0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:24:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:24:25 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:24:25 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:12:36 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:12:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dd3b27db5b90473cd40b6a58bd74aaa2fa2f05afe0691341705918804f631d`  
		Last Modified: Wed, 01 Mar 2023 05:28:30 GMT  
		Size: 1.6 MB (1566316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06944759ea3c71ed39cd35237ad73f9a26c9534182c600ce03dbba210f783d82`  
		Last Modified: Sat, 04 Mar 2023 00:17:02 GMT  
		Size: 198.3 MB (198274131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
