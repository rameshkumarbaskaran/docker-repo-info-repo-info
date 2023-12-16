## `openjdk:22-ea-bookworm`

```console
$ docker pull openjdk@sha256:f2e3462af093035043c981d16162b1f9cc80e3ee9f574c5c832991a50456676d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:2888ee4a8be94224e9d94e55895396f882453df60c8e4c2d2abd378b75942596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357554877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea1c2eea3eb0d0deb1cd5b339dcc53532751fc65530f95a8121d26a8d0c9208`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:52:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e1a8ca91d35598fbae8dee7f1c211f0f93cec529f6804a60e9301c53a604d0`  
		Last Modified: Tue, 21 Nov 2023 10:01:22 GMT  
		Size: 24.0 MB (24049172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a767d1d12e57724b9f254794e359f3b04d4d5ad966006e5b5cda78cc382762`  
		Last Modified: Tue, 21 Nov 2023 10:01:41 GMT  
		Size: 64.1 MB (64130771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c85fda2deed223e59393bd9b5b5005fc9c5d506d59a6367209150d15752da`  
		Last Modified: Sat, 16 Dec 2023 01:52:14 GMT  
		Size: 16.9 MB (16949229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe81dee7a42e57a28d071b1cc896c676174860bd055da3b4d73f8e5c8573fdf2`  
		Last Modified: Sat, 16 Dec 2023 01:52:18 GMT  
		Size: 202.8 MB (202843480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d14e4e6384d888ec1bcd3bc6becd630bd2858f538bbe38f88d71dcbc10436f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e215ea05fc659715f61c36ce42670855c3c2050cd6fa0ac6f978b5ab43e1ea`

```dockerfile
```

-	Layers:
	-	`sha256:0736941cf3e562d17d29e5724b1b46da29d152e1b5c886ff9d5a4925d18ca0a6`  
		Last Modified: Sat, 16 Dec 2023 01:52:13 GMT  
		Size: 7.1 MB (7116216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2f5148d515af8170a6209474b404cf5cf54e757ca818c9595d689b2ef88af0`  
		Last Modified: Sat, 16 Dec 2023 01:52:13 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:78f3145fa70b24e30974730cd6d09bae49b62f99b588180cc56e13636f030463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355820700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e49a334bc4cb5d6c21d671840080b8b93dddb0ff4e3135d2593495a682485e6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:57:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d647f1dd7e741209a8a75083ccc889e39cb3e94c17f45441eae96e1a679d971`  
		Last Modified: Tue, 21 Nov 2023 08:06:01 GMT  
		Size: 23.6 MB (23584876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdd9a70365f741a6b9f7a4e32cdb7d4aa29ac73da0b78ca0a83e937f285fdd5`  
		Last Modified: Tue, 21 Nov 2023 08:06:19 GMT  
		Size: 64.0 MB (63994275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc6ea26c20f1b5bc02a72a1735a76f0ae863509017fa522e313126696dc52cb`  
		Last Modified: Fri, 15 Dec 2023 23:22:25 GMT  
		Size: 17.7 MB (17732314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab9a5c2529cc6bbfee8717bea659546e109dc537154e03b8c148b4aa1d203e`  
		Last Modified: Sat, 16 Dec 2023 19:16:27 GMT  
		Size: 200.9 MB (200896585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ed08a9ccf61e8e9b5f35ea5919afeef1efba977348ea9c81b387729120fbfa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39182184ebafd02a4597da0bd6e848b38a31e9b99b286e1ae5cec2f2fc1dd7c`

```dockerfile
```

-	Layers:
	-	`sha256:9317a431947ce9909d80fcb2b2d1647830d69322cb2a3ae0e00238ff6021efb2`  
		Last Modified: Sat, 16 Dec 2023 19:16:22 GMT  
		Size: 7.2 MB (7235043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5890393df8575d96251be32cb247a2c4878bb09041ec07f187d53bfd55280f47`  
		Last Modified: Sat, 16 Dec 2023 19:16:22 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
