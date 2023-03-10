## `openjdk:21-ea-13-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:b2b9e06b6b87be70522d7903d641b0d8a7aa25de00709c9982cbf6d613a6bf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-13-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e4a3bdabc7648f608c03c6b661e05aa1b0d16858d5e7c064f3158135f65760d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232905351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcaf591eb20baf4dbdff0409cfc12aaa59b4020d32f4a36e9841b871960f163`
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
# Thu, 09 Mar 2023 23:27:20 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:27:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 23:27:35 GMT
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
	-	`sha256:8c155c73f41781f296dc48919ad04a9a4bda0ba8d3d085075f48e578ff610555`  
		Last Modified: Thu, 09 Mar 2023 23:31:44 GMT  
		Size: 199.9 MB (199911641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-13-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:96c5f26fbcea8213ec4c7318e34fe19329d642ff7d4afd0fa991017ed8cb36de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230041822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fa9a95ea17ae1535def0c05b5d7672c4acf39f82af46bc1a2e965bf60d3f9e`
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
# Thu, 09 Mar 2023 22:47:42 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 22:48:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 22:48:09 GMT
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
	-	`sha256:09599d44c1b94ee87699f78aa162b484bcc750fec89b0b56d69df9ecbe69e6fa`  
		Last Modified: Thu, 09 Mar 2023 22:52:04 GMT  
		Size: 198.4 MB (198412692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
