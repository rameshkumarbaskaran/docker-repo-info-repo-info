## `clojure:openjdk-18-boot-2.8.3`

```console
$ docker pull clojure@sha256:94040b4c7d00b203d4bc1763d02afe0574e949972a214f2225d9d5669483f810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:29fed8ea231036d8a339a8addbfc37aa50f358d1cabf8166ebcf4cb6453e7c63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280333987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dac7794a8c96a2c13e7353505364fbbd66d8502efc06faf73af98268d4d351`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:21 GMT
ADD file:19d7ba0fceddd7fc78b5fb96cf8110e5d10e0e5d2554030dfe640d161379cb79 in / 
# Fri, 03 Sep 2021 01:21:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:31:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Fri, 03 Sep 2021 08:31:20 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 08:31:20 GMT
ENV LANG=C.UTF-8
# Sat, 25 Sep 2021 00:25:42 GMT
ENV JAVA_VERSION=18-ea+16
# Sat, 25 Sep 2021 00:25:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ec604f7aef23624c0acdc0db346a2b226aab47d120538833070f0d5e01d571c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='623eff3e61bd5f74442fb5699ac3dea167dbe0ade7dd6c1fa9cdd4788e316b96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 25 Sep 2021 00:25:56 GMT
CMD ["jshell"]
# Sat, 25 Sep 2021 01:21:51 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 25 Sep 2021 01:21:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 25 Sep 2021 01:21:52 GMT
WORKDIR /tmp
# Sat, 25 Sep 2021 01:21:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 25 Sep 2021 01:21:56 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 25 Sep 2021 01:21:57 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 25 Sep 2021 01:22:20 GMT
RUN boot
# Sat, 25 Sep 2021 01:22:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f8416d8bac72cefc0ce17bd2dc0c03aa43e123d309db92ee23be9382192cf2ed`  
		Last Modified: Fri, 03 Sep 2021 01:27:25 GMT  
		Size: 31.4 MB (31368702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ae0b0c4c13e1ebacfd091b8e226cc8aa92df8937632e3bec2b03a877bf2d87`  
		Last Modified: Fri, 03 Sep 2021 08:49:03 GMT  
		Size: 1.6 MB (1582002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90416dc6dd4ab7f0222694d32e64bba4e610c0cd0dcf2227cc3631e39d4f3ea0`  
		Last Modified: Sat, 25 Sep 2021 00:34:30 GMT  
		Size: 188.3 MB (188279789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025bf23355b61c491701aefff1d2f0b2188d61ca22f1064bb6f721618f129e27`  
		Last Modified: Sat, 25 Sep 2021 01:28:38 GMT  
		Size: 283.1 KB (283056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83878ca6030ca909ab97404119940b28eae5e779e69146d1af02ccaa37fb50f6`  
		Last Modified: Sat, 25 Sep 2021 01:28:41 GMT  
		Size: 58.8 MB (58820438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ddcad5ef97290157ff600877fe320a2b37a6e81a118adb586970a20d49abcad0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277587174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d43111042869a1075d869bc77b77e3ad85b2a796c2e31a6d4a96443070ec9e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:33 GMT
ADD file:9600a4686ae105acffa54787a7c81f5252e90023cbcfbe37519150b954110c5c in / 
# Fri, 03 Sep 2021 00:40:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 10:44:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Fri, 03 Sep 2021 10:44:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 10:44:30 GMT
ENV LANG=C.UTF-8
# Fri, 17 Sep 2021 19:17:26 GMT
ENV JAVA_VERSION=18-ea+15
# Fri, 17 Sep 2021 19:17:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/15/GPL/openjdk-18-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d04e7163eb9519d4c918acc60d1f92fd7b6ff28bb0a43d7019790590b120725c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/15/GPL/openjdk-18-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='7a154bf56a56e4c4a4cdc6b5542e916b81baca431de262fa1a07e07ca313bd5e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Sep 2021 19:17:40 GMT
CMD ["jshell"]
# Fri, 17 Sep 2021 22:12:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 17 Sep 2021 22:12:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 17 Sep 2021 22:12:44 GMT
WORKDIR /tmp
# Fri, 17 Sep 2021 22:12:48 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 17 Sep 2021 22:12:48 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 17 Sep 2021 22:12:48 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 17 Sep 2021 22:13:07 GMT
RUN boot
# Fri, 17 Sep 2021 22:13:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1901ca797b5ea06f6a4facc81ad772177fdd833ed4329dc86ef126078633b949`  
		Last Modified: Fri, 03 Sep 2021 00:48:51 GMT  
		Size: 30.1 MB (30055483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cacb51d4ac932821c4ef93d9b1b99d91b46e6936de614b998343b89d39ca977`  
		Last Modified: Fri, 03 Sep 2021 11:04:46 GMT  
		Size: 1.6 MB (1566199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3873ae9d8d29f778690ae082c9c69d432e2a7fbd380911e35cc4e27fdeb2a837`  
		Last Modified: Fri, 17 Sep 2021 19:33:04 GMT  
		Size: 186.9 MB (186862006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aefbe7d3b3c629ae301ba39ac7573ea3a2ac5432d158b482ca3e8dfb3ba1ace`  
		Last Modified: Fri, 17 Sep 2021 22:22:34 GMT  
		Size: 283.0 KB (282976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cba7f93c2f0c7c34a60a2c58e71fca9ba66f5e32481147c170bd1bd8b8d5004`  
		Last Modified: Fri, 17 Sep 2021 22:22:44 GMT  
		Size: 58.8 MB (58820510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
