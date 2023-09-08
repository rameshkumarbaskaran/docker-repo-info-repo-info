## `openjdk:22-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:a1adcc050991dd6e8002c68b5eb6f4339b3d6cfe1b5b924b1b6015592159ec49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:4ceacf41a844045cdffd0fbfb29e2336214e8160d7f1d0d3db47330ea3cc5b60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238326393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefc42523da91943aa60271b481e2ccbbd2f6d0e09abe8d81a68823475bf910f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:02:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 05:02:29 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 05:02:29 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 19:45:05 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:45:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='2d6b271eaaecdedb8eee2e64b7cca4f36000039d3bdfe618460424fb8e449fcc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='62b2cad2a14380255f3f0dee68193a8d2953c0b8cce04eae1f65427d4ab2b707'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Sep 2023 19:45:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d609f39f66b85b17d8f4adcc8ae8193d59115abe8cccb6cb3b92b7505dc49`  
		Last Modified: Thu, 07 Sep 2023 05:06:40 GMT  
		Size: 1.6 MB (1582422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b1844703872abf56a1064cf0c6da8bed820f80b4247ae457b9696bea54eab`  
		Last Modified: Fri, 08 Sep 2023 19:49:40 GMT  
		Size: 205.3 MB (205326468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5f3e426fc75d3ea071d46b678664d028b8051b89b778180baa419f1761d3d571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235220765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b0cc249bed3a814a1612207b903fdcffe04db0827f41a5065c24b6cb330ca8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:51:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:51:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 01:51:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:51:41 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 01:51:41 GMT
ENV JAVA_VERSION=22-ea+13
# Thu, 07 Sep 2023 01:51:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='fb110a662f4aaa988d446d09ec4ad4683cc96ee24d9f4ebf5c96177b441fa1f2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='d8c826ad7c22505872c310eb7651a071dc380ee14401b65b08861ec4ffc6b95d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Sep 2023 01:51:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04284697cdcc06052ec1cff605b74ea641c90e14dd4b9026a2ebc812c5a5625b`  
		Last Modified: Thu, 07 Sep 2023 01:54:22 GMT  
		Size: 1.6 MB (1566472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc71dd477047e14bafdc6ddc3246ce23b8572a93622a517298df5529fc5cfa`  
		Last Modified: Thu, 07 Sep 2023 01:54:34 GMT  
		Size: 203.6 MB (203591390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
