## `openjdk:20-ea-12-slim-buster`

```console
$ docker pull openjdk@sha256:4420abdc70ebad18e5d7eb50e8a260670827ef942324ecea454d9df372159f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-12-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:b96ff171cb535e0e83ce388d24a85c51f8c1eb9a1a5d8db9e3a0d1d79ce0f2df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228037923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397114004732f963ec9e8f7c6ab3135d7507337aea15de9ee42c03da425aa1bc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:30:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 04:30:24 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:30:24 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 21:45:21 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 21:45:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 21:45:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4bb2aa3cefa352eef3f71a4b1e2d70041ef3c1e9cf1b9802e5d43db17fcf35`  
		Last Modified: Tue, 23 Aug 2022 04:37:53 GMT  
		Size: 3.3 MB (3273368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be103ba89116c7a5992236dd5aaad6d4ecf1d883c89462de168950a51258c0d`  
		Last Modified: Fri, 26 Aug 2022 21:52:45 GMT  
		Size: 197.6 MB (197626225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-12-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8dd71ea43b7d862a3cc0fce991d8658a0d9c153f59512123aa844d953383b79c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224997492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46779cf3f92f280fd50ac8b1a7b0fa657a8d508c9f5fcd7e03bc5dc9b480e923`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 05:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 05:17:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 05:17:34 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 05:17:35 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 22:06:03 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 22:06:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 22:06:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356227960c8e171a8438469fe7c95bc6d10c5694b55ced0cb37aaaabaef7f2dc`  
		Last Modified: Tue, 23 Aug 2022 05:29:25 GMT  
		Size: 3.1 MB (3126086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242be821a01000b16991548ceddd9ff8945d467d55b08bedbd0279b50e97e604`  
		Last Modified: Fri, 26 Aug 2022 22:17:00 GMT  
		Size: 196.0 MB (195958891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
