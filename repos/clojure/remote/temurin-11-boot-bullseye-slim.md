## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:3c6600a397eae75aed8f7f400ce5939b44d360b2b21a3a6fbb50adbf28634386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c76278dc2967712a1ef81af5ce82358250d2a71237d49bf2712fd97c980f7a1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236584586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9567936e17e18ea2240ae7217e47fdeb41455be16b27b7bb9208bda11a9116`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:18:55 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:18:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:18:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:18:56 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:19:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:19:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:19:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:19:19 GMT
RUN boot
# Wed, 01 Nov 2023 01:19:19 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0c2457a667e342734343cd296f94de2032329a37ee32ca0f48794427a59f05`  
		Last Modified: Wed, 01 Nov 2023 01:37:19 GMT  
		Size: 145.3 MB (145266641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63118a3aea10b17cf9c7eb91f79972ef25ec7139784ce5684b76fdb5aee57056`  
		Last Modified: Wed, 01 Nov 2023 01:37:07 GMT  
		Size: 1.1 MB (1079485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d47d1ea10bee08bd5f623ed2570c58317542824263da059c00cc0f532665ce`  
		Last Modified: Wed, 01 Nov 2023 01:37:11 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbb59e38714e52ac1ff01d25d0d5b743da1c31a7a350fef157d1e4ce3f859881
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231953377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ad5b6df14a588ef74cf447beb11d2fbfa141a15a4c1f04b15d7766bcfd5746`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:58:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:58:33 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:58:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:58:33 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:58:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:58:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:58:38 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:58:55 GMT
RUN boot
# Tue, 31 Oct 2023 00:58:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400bc1a1e493a334894d45d828e4a5ac8f80587e9ffc23358e025523917e71d8`  
		Last Modified: Tue, 31 Oct 2023 01:18:08 GMT  
		Size: 1.1 MB (1066860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70de89fd25429f86313ed6d2191e628628541db1f2b346c93e9501106893e5`  
		Last Modified: Tue, 31 Oct 2023 01:18:11 GMT  
		Size: 58.8 MB (58820477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
