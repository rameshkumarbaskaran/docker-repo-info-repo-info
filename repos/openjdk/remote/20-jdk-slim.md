## `openjdk:20-jdk-slim`

```console
$ docker pull openjdk@sha256:d47f9b0ee597f0226664bba4b8338e86c5aac9b088c9c8c1d98f129b8ac5d2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:71ff0f80478fe267e1402be75ff40946ac9cc120c2a6343315fae05516fd991c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230589199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38341c2a78d287e10711f8ef454aabdb441e80aa056f53cd664d12a796c841`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:29:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 04:29:36 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:29:36 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 21:44:47 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 21:45:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 21:45:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b1c853f5d1e2529f16cddde75874e53c112a9bee4b0954afb1bb8a2a29044b`  
		Last Modified: Tue, 23 Aug 2022 04:36:30 GMT  
		Size: 1.6 MB (1582289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf62a6c5e120b33957b76468b059a8dcea324d6dc3ad41a4c22b73cf30699df`  
		Last Modified: Fri, 26 Aug 2022 21:51:23 GMT  
		Size: 197.6 MB (197625425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4f7e05a6a537ff523470e6e6bdf6def1e294dfc1fc13908fa2e6aa0db7cae415
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227379367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720448bc7851a9a8d1e8e40b4acd00fb7572e341031a8067273ad4b9bc432bb2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 05:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 05:16:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 05:16:06 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 05:16:07 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 22:05:18 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 22:05:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 22:05:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336c8a0edb35428a570e25d2023ce4e03a37c1c31638892cc2c38fca7cf3c91`  
		Last Modified: Tue, 23 Aug 2022 05:27:39 GMT  
		Size: 1.4 MB (1361214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1fc770ded9029cb4328fc9f27b4bcb1571649dac31309cac23e074d5de6089`  
		Last Modified: Fri, 26 Aug 2022 22:15:21 GMT  
		Size: 196.0 MB (195954365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
