## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:e504abe4d7ba8fb97a242efd86fbea986a6de4c991eb482f350e7bfebf087644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d1d61fd37a649d3cda02a8ca50d3508c093cef8c3517603576bf4073e0fe906d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236141633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a6ff7a5385f749d4b347376d4cf3791823605b385eb2e9e83d42dcfecfd6ed`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 02:04:50 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:21:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:21:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:21:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:21:27 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:21:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:21:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:21:33 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:21:52 GMT
RUN boot
# Thu, 07 Sep 2023 03:21:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2204a29ef2517e9d39b89552fcfbd45063a2d758626e1aef118a701134c2d`  
		Last Modified: Thu, 07 Sep 2023 02:07:35 GMT  
		Size: 144.8 MB (144826055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bb3fc1e9accf2b4c731f8192c44372f9f3948737a1cd2d069d477c725d4426`  
		Last Modified: Thu, 07 Sep 2023 03:31:33 GMT  
		Size: 1.1 MB (1077548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b12b1ef07ecbb22e7c859f3c98ecfa1ec57a96d529e31b9be42def5fef40602`  
		Last Modified: Thu, 07 Sep 2023 03:31:36 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:119dc9699549818833ab18f4b2b6bde9b83470a7ae06823b8bf645254499648b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231518558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a517ea0b09f7eb1394516016085dd4d5088fb3f324c92e7bda0e68c66132b7e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:44:25 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:44:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:44:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:44:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:44:29 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:44:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:44:34 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:44:53 GMT
RUN boot
# Sat, 02 Sep 2023 01:44:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b924b77d195ee682d4adf6c744cba3a607633e56b93e8e8d9161e1a29b17fc4c`  
		Last Modified: Sat, 02 Sep 2023 01:53:29 GMT  
		Size: 141.6 MB (141570383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52456ab1a7b8f3e40dc2f5930b0b715cac5442cf29aa839c059cc1d68272d66b`  
		Last Modified: Sat, 02 Sep 2023 01:53:21 GMT  
		Size: 1.1 MB (1064876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e52705d096e8881848a5becc6b8ff6fd77725844aa6f96e0ec4f39fbf70d6d`  
		Last Modified: Sat, 02 Sep 2023 01:53:23 GMT  
		Size: 58.8 MB (58820483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
