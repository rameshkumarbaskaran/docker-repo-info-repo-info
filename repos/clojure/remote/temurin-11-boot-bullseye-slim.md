## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:c0507c0856363172133b354390938ac020b3bbdb234cbe1c2052ee79f294f4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ec2f379661bc23cf30afd026ad25196cbeb2e396b650630bc980368f87f8904e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289770326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3b68be362012ac62445cf82cffd8b4ee5fd16c3187be6b4dc6da34ca60988`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 03:12:45 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Feb 2023 03:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 03:12:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Feb 2023 03:12:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Feb 2023 03:12:47 GMT
WORKDIR /tmp
# Wed, 01 Feb 2023 03:12:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2023 03:12:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Feb 2023 03:12:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Feb 2023 03:13:12 GMT
RUN boot
# Wed, 01 Feb 2023 03:13:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899461231daebed67afa81449e6f387d18128daf428198d59ce67487ecb2845`  
		Last Modified: Wed, 01 Feb 2023 03:30:42 GMT  
		Size: 198.5 MB (198475511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d3609cad038e7faf7104ffdda909d5b61c357d7261e63df76e2db8fe784d`  
		Last Modified: Wed, 01 Feb 2023 03:30:27 GMT  
		Size: 1.1 MB (1077368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e18aa1ace6f0d3eeac4ed1cc56fcd59510bd45a71c8599c30c2eb1470898ad`  
		Last Modified: Wed, 01 Feb 2023 03:30:30 GMT  
		Size: 58.8 MB (58820475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8345d176b31933170ba4155143158dacf8d8a19b5cdd2ab6efd29f197c7d9c71
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285170253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e1a0e8ed0ea783714bf81011610059f12aaf0dea23f9889f0e8941cd416ab9`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 20:50:12 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Tue, 31 Jan 2023 20:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 20:50:16 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Jan 2023 20:50:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Jan 2023 20:50:16 GMT
WORKDIR /tmp
# Tue, 31 Jan 2023 20:50:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Jan 2023 20:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Jan 2023 20:50:22 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Jan 2023 20:50:40 GMT
RUN boot
# Tue, 31 Jan 2023 20:50:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5842b36268c5c5b9539a446d9eba4513a75b1955de0b698663ccf059458ac527`  
		Last Modified: Tue, 31 Jan 2023 21:04:34 GMT  
		Size: 195.2 MB (195240302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e435c5f718cb8031f50e14c7fe179028adbc439627711fe2846fd44e7fe708`  
		Last Modified: Tue, 31 Jan 2023 21:04:22 GMT  
		Size: 1.1 MB (1064677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52058ee7835930862313ce34be594de169216362f1f45e4872cd7b3e5e3aa55`  
		Last Modified: Tue, 31 Jan 2023 21:04:25 GMT  
		Size: 58.8 MB (58820460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
