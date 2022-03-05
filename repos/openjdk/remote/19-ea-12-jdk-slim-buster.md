## `openjdk:19-ea-12-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:360ff2b54931cf0fa37f36243f4c8726bb99819127f0cd088d14ae42e90f8f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-12-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:f4ca0e0e1adaeaf774a958b2f2dfbb8d854054d9c89f1a76c3fa4ca3e196b5ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223861676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a51188ad540cd7f9917a4eb630f7332be34a235353300783c5490634175ee`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:22:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:22:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:22:12 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:22:12 GMT
ENV LANG=C.UTF-8
# Sat, 05 Mar 2022 02:05:16 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:05:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:05:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1727fec028eb22f37a4c93bbb31a582ebabb7664730fb7f93179214d45b7174`  
		Last Modified: Tue, 01 Mar 2022 14:42:23 GMT  
		Size: 3.3 MB (3269641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45148bccb060564214f41cfa79d0436962ef1cb1eb5007dd04dad274a2880d5`  
		Last Modified: Sat, 05 Mar 2022 02:14:55 GMT  
		Size: 193.4 MB (193438298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-12-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:809aa8994f77ed861dbe92c0157c0454391c0fda00368f94322162452ea83992
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221291197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46de616cf07132b262e67e6024161c308a996db22164c024f2d4b1117615072c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:49:25 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:49:26 GMT
ENV LANG=C.UTF-8
# Sat, 05 Mar 2022 02:57:08 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:57:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:57:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1598aa0249d59bdc58f96c0187ae665625594bf9f256f5bca2c1b941fc493be2`  
		Last Modified: Tue, 01 Mar 2022 14:14:40 GMT  
		Size: 3.1 MB (3118853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a45b3ac350f11321bcabce38a3f5e78a19d3dbef72620de771c17b591c5effb`  
		Last Modified: Sat, 05 Mar 2022 03:12:48 GMT  
		Size: 192.2 MB (192249204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
