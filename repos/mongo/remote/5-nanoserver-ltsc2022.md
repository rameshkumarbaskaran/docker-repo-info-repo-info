## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:531adc94da28407ac94608f29cd37fad71762eede84083d0861e425a0b9d19e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:1b79e81a346ab6ece8a7f3dea1acdaf87964dfa06fdaf7fc6d83bb38b148ccb8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.0 MB (432977652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71019ed35e6cd5f667383508eeba68260cadb159062ede3afae4985fb23502be`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:39:21 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 01:47:25 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 02:31:26 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 02:31:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 24 Jun 2023 02:31:42 GMT
USER ContainerUser
# Sat, 24 Jun 2023 02:52:25 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 24 Jun 2023 02:52:26 GMT
ENV MONGO_VERSION=5.0.18
# Sat, 24 Jun 2023 02:52:52 GMT
COPY dir:ab74dbf9ad27d2154a3f270894c5c95f10fe56a2d5ec4c1875a57c2afdba8cff in C:\mongodb 
# Sat, 24 Jun 2023 02:53:05 GMT
RUN mongo --version && mongod --version
# Sat, 24 Jun 2023 02:53:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:53:07 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:53:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d6e77b89ecdadfdd3ef274e9a235590c9cd4dc832939932eff32f93250571005`  
		Last Modified: Fri, 23 Jun 2023 07:43:32 GMT  
		Size: 120.0 MB (120028254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2deb8649e4dedd9fbe74195175cfdae8176065d0daa61337779d26f0bce93`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c851c15426494687424d4597399ac88799abfe339928d85f4df7a6abdbed5ffc`  
		Last Modified: Sat, 24 Jun 2023 06:32:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9545ffe158e5ffac274b8e7c5297117a1f8983e3a4e95d6a8baffe412d1b51ef`  
		Last Modified: Sat, 24 Jun 2023 06:32:14 GMT  
		Size: 80.6 KB (80567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c836921d67898e578c9bc0af8cd07ff59136154efb53925baca8c19bed341989`  
		Last Modified: Sat, 24 Jun 2023 06:32:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a1f9cf9505113f36b7171be921a9786923b3da255d62cb98bdbb5967c4c290`  
		Last Modified: Sat, 24 Jun 2023 06:49:22 GMT  
		Size: 263.5 KB (263506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba2bd85d1c6d07fd0d50ce0c58b7d0b01fcdb88aaa6e9e5a6abbffd57902879`  
		Last Modified: Sat, 24 Jun 2023 06:49:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51a18c88bf9e689041ea4100ed0e6484c3d965eeecee5d9f7493fa023867505`  
		Last Modified: Sat, 24 Jun 2023 06:50:12 GMT  
		Size: 312.5 MB (312540150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e29a5c3592afe48918ee765846c491dd38cf4f4d45f8a94ba720f30a69e2dc5`  
		Last Modified: Sat, 24 Jun 2023 06:49:20 GMT  
		Size: 57.2 KB (57169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc9917b7e132754d40e2c6f27e3674ca228ad6d08f2592c040ed0dd4461914e`  
		Last Modified: Sat, 24 Jun 2023 06:49:20 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5728d8d7b4256dfe61eed5240c53282ee7b71f9501d60fd2fb771ded0c0b81`  
		Last Modified: Sat, 24 Jun 2023 06:49:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca8d7085043f54fc44c0dabb38d3eb9f31cf0e77a68ba39e5aaacae1544bd3`  
		Last Modified: Sat, 24 Jun 2023 06:49:20 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
