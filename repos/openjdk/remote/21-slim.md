## `openjdk:21-slim`

```console
$ docker pull openjdk@sha256:1cb61bc1564a391a8a49b97a17f992dfa409990002436aa19be89b47ab11f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:58b6a71935e33dc39785423027a6f957c749f74eeb90b7937587c27fa4f5cab2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232435901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9d78a4f8c62ef3214ee7544468244d19a8adb418c1da1a492ef7d5c9d58f37`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:10:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:10:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 12:10:31 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:10:31 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jan 2023 19:22:32 GMT
ENV JAVA_VERSION=21-ea+4
# Fri, 06 Jan 2023 19:22:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/4/GPL/openjdk-21-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='b0b66696997381f01795b6c1b7fcd9eb54369ec5603ae627f77cdadf00e13432'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/4/GPL/openjdk-21-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='17592e76ae98f20777ab47e086d420ae2cd937e62d6ff9cc49619b673a5bc9e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Jan 2023 19:22:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc03ebf496347487b6180d378e9c5769b292b90df671ddc991422926d0809fec`  
		Last Modified: Wed, 21 Dec 2022 12:17:41 GMT  
		Size: 1.6 MB (1582327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d51c68de6b010f03009b2847f9602c7343fbf27effcb4e5667eb77d2341912a`  
		Last Modified: Fri, 06 Jan 2023 19:30:15 GMT  
		Size: 199.5 MB (199456631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c47dc210725f2096e6190ecc9446dd545ab81caba36721e08efeb57dc1a3a34a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229511423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42956af70fa15e68eda4356e953ea3b0b5b655bcf180fa6be8f07bc7f0adeedb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:53:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 03:53:33 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:53:33 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jan 2023 21:40:31 GMT
ENV JAVA_VERSION=21-ea+4
# Fri, 06 Jan 2023 21:40:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/4/GPL/openjdk-21-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='b0b66696997381f01795b6c1b7fcd9eb54369ec5603ae627f77cdadf00e13432'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/4/GPL/openjdk-21-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='17592e76ae98f20777ab47e086d420ae2cd937e62d6ff9cc49619b673a5bc9e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Jan 2023 21:40:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25ec39ac4d8c95008c4cae68bf15b8d0f09df7a1b2b0b0c892724ec59abbd2`  
		Last Modified: Wed, 21 Dec 2022 04:00:05 GMT  
		Size: 1.6 MB (1566279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299994f8e5739166f97ecddd4e3e5b828655d6bab5f4ebcc236f86bb473c114c`  
		Last Modified: Fri, 06 Jan 2023 21:47:58 GMT  
		Size: 197.9 MB (197900372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
