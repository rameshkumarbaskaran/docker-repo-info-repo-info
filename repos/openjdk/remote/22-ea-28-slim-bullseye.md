## `openjdk:22-ea-28-slim-bullseye`

```console
$ docker pull openjdk@sha256:af3e171571c5ee9f6621aab98a2088422c0c03837ca6ddbb15bfafd19736b6d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-28-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e661a0db63ce5fc56b8219c7616954ebecd6929d27a6be708238f4cb782ba9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235684257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd8b428ad90023ce0c72e6cb0b3c701bf9eafdf4ddb844f4710756959007de`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16225f69edaceefe12ee215f27d353e48f4247b77f5407dcf3e52c036c92a7dc`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 1.4 MB (1378145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d5b1171d9fc53378a1a0c3e6a54b302cc620acf203c32d11ae8b25d6d5aa72`  
		Last Modified: Sat, 16 Dec 2023 01:52:01 GMT  
		Size: 202.9 MB (202888288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-28-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:05bfedc22072489cd6037ac87e276b6bb00b0a6ff0c20f5cacb101b02e51843a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889ac2b921fd1b164598fe2e7af39da35776b0215254931a091268eb511b6d7`

```dockerfile
```

-	Layers:
	-	`sha256:2201969f1caa5d3716ed56938a78e88c69d1635b58801c7d6db04329213e23cf`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 2.2 MB (2190189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b5d02baa743b17d2c45e5f3ee134835236c8492acbf4aa82d0def0d7d25000`  
		Last Modified: Sat, 16 Dec 2023 01:51:57 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-28-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:37d06e305418ec1ed616cbf945d9dfb0a1784226758666ed4ebb09e04ffbd955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232370348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0eedf18d49c9dda9dc18a7c536acb81c1e21c4a47c3f573df587094ee8e2f97`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b44bd09e3f229b14cf1e2425e653e0398d79b3eb82f0a7052b42ecf74ba27`  
		Last Modified: Fri, 15 Dec 2023 23:26:07 GMT  
		Size: 1.4 MB (1362043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf444152fcfb2c3243569da99ceb6740e90901b3f43a5f62a3ec91df6507fc3`  
		Last Modified: Sat, 16 Dec 2023 19:19:00 GMT  
		Size: 200.9 MB (200944182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-28-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bfa2ecb5356e86d8735eaba8f850d14eb2c67021b7b883e07f8d7b92b7aae9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e8361d8764af8acbe1739e79783b6305ee3bf480e4e201904cba7c9ad84c5f`

```dockerfile
```

-	Layers:
	-	`sha256:e96e65095bccac886ac628c867e90cffb949871e6d447793534bfd4741b960b0`  
		Last Modified: Sat, 16 Dec 2023 19:18:55 GMT  
		Size: 2.2 MB (2189547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a637cab0f7576c781267c1026fd442122dda446f8a7b250c0472d75184bf066`  
		Last Modified: Sat, 16 Dec 2023 19:18:55 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
