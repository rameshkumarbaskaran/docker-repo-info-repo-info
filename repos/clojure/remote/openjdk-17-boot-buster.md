## `clojure:openjdk-17-boot-buster`

```console
$ docker pull clojure@sha256:dcc91c9e9791dad5eb9970a2b8ec0f8d14bd24ebb1ef1bb86a4653e6c9a0ffd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:14a3f4d9e5bac418ee1b8a6922b9e5570b884c249fe8425af6419d1bfe0d2ac9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380119105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f62cac98614928dcf14043389e074f8bd4cad1184e2169ebf5b7f4c7c0dd8f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:47:27 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:47:27 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 21:23:21 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:23:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:23:33 GMT
CMD ["jshell"]
# Mon, 14 Jun 2021 21:52:34 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Jun 2021 21:52:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:52:35 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:52:36 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 14 Jun 2021 21:52:36 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:52:36 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Jun 2021 21:52:55 GMT
RUN boot
# Mon, 14 Jun 2021 21:52:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53c8574903f2e47274cfe45903823235a9b4b846f7771f2a75a8e6a1462162`  
		Last Modified: Wed, 12 May 2021 06:57:35 GMT  
		Size: 13.9 MB (13921268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd7155a2a32dac35425336b4b89820a94c305fae93a42e5dd293bf7b4bc7584`  
		Last Modified: Mon, 14 Jun 2021 21:32:50 GMT  
		Size: 187.3 MB (187265678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c69ecd784304f8382541d071fa34d98adf6ca79182770348db485ba56b1eac`  
		Last Modified: Mon, 14 Jun 2021 21:56:41 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4956f22d52ec6b425bc45dc78db66130de7d74fe112a8fe14367fa73c93fea`  
		Last Modified: Mon, 14 Jun 2021 21:56:45 GMT  
		Size: 58.8 MB (58820432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a5f8a30ae244cc77e165101109dd4108ce4c570bba5d381fba2ac34e9b82e04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378663121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f14579314fcc67bfe8fa85425049374cee9326418b90464c4178294624b9d0d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 20:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 05:20:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Fri, 28 May 2021 05:20:03 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 05:20:03 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 20:45:02 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 20:45:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:45:12 GMT
CMD ["jshell"]
# Mon, 14 Jun 2021 21:23:36 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Jun 2021 21:23:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:23:37 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:23:38 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 14 Jun 2021 21:23:38 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:23:38 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Jun 2021 21:23:57 GMT
RUN boot
# Mon, 14 Jun 2021 21:23:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8aff564b222789ed2823b88e0f1a69ac00cbcbf9349acb8a363d5ef9724182`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e893e0778bb86166fb6799aec4e4ac337c4f10172386c8ae9cf3c787331d7d`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 10.0 MB (9984325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf2dd6193dae84aecaec1d65081288ca49fe0843460035cc060b5aa4e7a9a7`  
		Last Modified: Thu, 27 May 2021 21:05:39 GMT  
		Size: 52.2 MB (52167766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e4f34f8162390a1c3755bde6c4b80914f4d5f6e0b090336929fcc052d69dd1`  
		Last Modified: Fri, 28 May 2021 05:32:23 GMT  
		Size: 14.7 MB (14673533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d2e9bc66b99d5bca8fd1e4fcc0ff672a7b71372d0a907d643971247bdf8464`  
		Last Modified: Mon, 14 Jun 2021 21:01:08 GMT  
		Size: 186.1 MB (186089962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79bc8c1f973f2934308c0e48f9b9d5d6002d3919ad23f06885e9c1c3ec2b06`  
		Last Modified: Mon, 14 Jun 2021 21:29:25 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62193658f07e5a76d9e5e16bd4c493aea79ce4e2636bada897400deaf700043f`  
		Last Modified: Mon, 14 Jun 2021 21:29:30 GMT  
		Size: 58.8 MB (58820359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
