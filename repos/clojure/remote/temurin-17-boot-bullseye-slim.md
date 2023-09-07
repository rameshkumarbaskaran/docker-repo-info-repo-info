## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:b7f7a538683548267e58164a914ce2e148d0c66d580cbdbfe10eea377f5b4ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:487f07fae61b71afc12d6ec7727c01917d3ebbad92bafab18d0eb41909cb588d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236091753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3db47bf2a0969944b82779dd6b6d6992dedc94ae326914c055f9f3591cc899`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 02:03:47 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:24:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:24:14 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:24:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:24:14 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:24:19 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:24:19 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:24:38 GMT
RUN boot
# Thu, 07 Sep 2023 03:24:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:24:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:24:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d09690feda2ec5aced0543a2cf8ee1aadf1e05dd333f551cc4b11eaa287a0`  
		Last Modified: Thu, 07 Sep 2023 02:06:03 GMT  
		Size: 144.8 MB (144775798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0cfeaf959e4e0d89cea5495403e174ff58b9951b4a7051ab33dfa0c9d82185`  
		Last Modified: Thu, 07 Sep 2023 03:33:17 GMT  
		Size: 1.1 MB (1077552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd29084fdc212089aba6195cbbc4ca89c335fd0c4cd1c135be65970957500cd`  
		Last Modified: Thu, 07 Sep 2023 03:33:20 GMT  
		Size: 58.8 MB (58820502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf4e8d8445e38b694a0728acd12a67edb9f6ea6e160234eee7ce7f25eda02a2`  
		Last Modified: Thu, 07 Sep 2023 03:33:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14e0d778dbcf89f0cbded29a619e74e9e948accaa74993665ddefb07636b9655
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233492105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac48bbbc0017a9ebee9cd2108eed9bd0d5e514bf3411db264d8f0a1ff1b07f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:48:00 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:48:04 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:48:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:48:04 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:48:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:48:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:48:09 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:48:25 GMT
RUN boot
# Sat, 02 Sep 2023 01:48:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:48:26 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:48:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75390d7bc4a96162e240272aeff28881955f7af498179aa85faecd879748f913`  
		Last Modified: Sat, 02 Sep 2023 01:55:46 GMT  
		Size: 143.5 MB (143543515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6609d00c40d78b8dfbbef7aecbccb296e31409a782e41d7c2eb33229765bdf6`  
		Last Modified: Sat, 02 Sep 2023 01:55:37 GMT  
		Size: 1.1 MB (1064830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c463f0425e6740b6d9abdb541b3a8129352472b86b9506031c099ef10da4c69`  
		Last Modified: Sat, 02 Sep 2023 01:55:39 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fe3c7d5e4d5ae1b7c61d7bd7c47f88113b7f6ae2d6f9540d47f8b1a29b5e17`  
		Last Modified: Sat, 02 Sep 2023 01:55:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
