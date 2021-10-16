## `clojure:openjdk-18-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:a7c32863fc7b9ec603bfc1887dea76f457a438389680c84f210b12f4ac4a0141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:786a2077b05bd9023c93d90819cf0c53c21246bb24b40021d6e6c2887d7ed959
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386432204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921c066e5bfcf8748e322a79981ce670646d5e350890cb60330326d2a57f4a9a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:42:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 15:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:27:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 12 Oct 2021 16:27:22 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:27:22 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 00:25:43 GMT
ENV JAVA_VERSION=18-ea+19
# Sat, 16 Oct 2021 00:25:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/19/GPL/openjdk-18-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='42b5b8f65bed00be3fa810f876581eb1cd5eebcfe44dae0361e9f4128ec905cd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/19/GPL/openjdk-18-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='518af06c8ba2d135a7ba43a937f1ed061e7d6acf55dc296cef60b1fd50413438'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 16 Oct 2021 00:25:54 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 01:30:12 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Oct 2021 01:30:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Oct 2021 01:30:13 GMT
WORKDIR /tmp
# Sat, 16 Oct 2021 01:30:14 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 16 Oct 2021 01:30:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Oct 2021 01:30:14 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Oct 2021 01:30:40 GMT
RUN boot
# Sat, 16 Oct 2021 01:30:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b617c6a8c415a175f44d7e2c5d3b521059f2a6112c5f022e005a44a759f2d`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 5.2 MB (5153273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e17419b7ee61bbd89c2f0d2833a99cf45e594257d15cb567e4cf7771ce34a`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 10.9 MB (10871935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d2d81226a43a97871acd5afb7e8aabfad4d6b62ae1709c870df3ee230bc3f5`  
		Last Modified: Tue, 12 Oct 2021 15:53:13 GMT  
		Size: 54.6 MB (54567761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbae81fdbbf50b4f75c539f7e4ab9fa83b3fbad9f297ed467c5b05cae3a83872`  
		Last Modified: Tue, 12 Oct 2021 16:42:23 GMT  
		Size: 14.1 MB (14071834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62e099f3c1ee096f013f91548aaf71a1ab345658df8712fb6618f09f6c8765`  
		Last Modified: Sat, 16 Oct 2021 00:33:46 GMT  
		Size: 188.0 MB (188022455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76de0bc3879cdd1472eeb6756960b8ee374ccba1d3022615b8005001a9dde0cc`  
		Last Modified: Sat, 16 Oct 2021 01:37:45 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfdc9dd19421c1446db0341a5a2bc48769b63f81ac334a2ae72ea7e38fe4fae`  
		Last Modified: Sat, 16 Oct 2021 01:37:49 GMT  
		Size: 58.8 MB (58820508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a84a7d4bc141c918edf0c62cb9c22837cc80edff74e1bf2f6c874eb41a6793c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385358292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f938a90138e8afe304520a33158e9ef64ee8f186b6d34fd6c66d6f0dca86d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:04 GMT
ADD file:1529ae12e334fd992892d3fb97c103297cff7e0115b0475bec4c093939a2bff7 in / 
# Tue, 12 Oct 2021 01:41:04 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:58:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 02:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 04:06:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 04:06:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Sat, 16 Oct 2021 04:06:30 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 04:06:31 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 04:06:32 GMT
ENV JAVA_VERSION=18-ea+19
# Sat, 16 Oct 2021 04:06:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/19/GPL/openjdk-18-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='42b5b8f65bed00be3fa810f876581eb1cd5eebcfe44dae0361e9f4128ec905cd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/19/GPL/openjdk-18-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='518af06c8ba2d135a7ba43a937f1ed061e7d6acf55dc296cef60b1fd50413438'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 16 Oct 2021 04:06:52 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 14:17:41 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Oct 2021 14:17:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Oct 2021 14:17:42 GMT
WORKDIR /tmp
# Sat, 16 Oct 2021 14:17:44 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 16 Oct 2021 14:17:44 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Oct 2021 14:17:45 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Oct 2021 14:17:58 GMT
RUN boot
# Sat, 16 Oct 2021 14:17:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1c47a423366578e5ce665d03788914bf0459485a627a27896fa9c5663ce55cdf`  
		Last Modified: Tue, 12 Oct 2021 01:47:41 GMT  
		Size: 53.6 MB (53603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b1f128be8ebd64f787c46418ffe34ce1096d1ccd6938924d7397713720758`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 5.1 MB (5141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c338d42ad921985fb8ebb6e2c48d381f6e03a91535eeffce7f08084b3dfbfdf4`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 10.7 MB (10655847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27d3d9a061af78e3fcbefe5dbbe718db380687319e5ba8a7c9fd7ba55d16cc3`  
		Last Modified: Sat, 16 Oct 2021 03:14:43 GMT  
		Size: 54.7 MB (54669931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6184c33cbbd3e136683d125fb9cef775eb12f0f0e3140a8edc23406be025a964`  
		Last Modified: Sat, 16 Oct 2021 04:21:52 GMT  
		Size: 15.5 MB (15524863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dddc07a8c355a94f1d0ea9de10d3466156e37e8822f4e661113a521dadf0e5`  
		Last Modified: Sat, 16 Oct 2021 04:22:07 GMT  
		Size: 186.9 MB (186940195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc88ab9e8c5286d1b0b2ba08c7643d0e4891595d20666a71967b36cbc174647e`  
		Last Modified: Sat, 16 Oct 2021 14:32:13 GMT  
		Size: 6.9 KB (6899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fd4c3950d090670fcb36b9a71e238ab479cbfa4e489091dbd745fdd085cc81`  
		Last Modified: Sat, 16 Oct 2021 14:32:19 GMT  
		Size: 58.8 MB (58815681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
