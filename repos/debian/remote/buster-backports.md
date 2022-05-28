## `debian:buster-backports`

```console
$ docker pull debian@sha256:9d72e51672da55e00a8a3c7edc4022873d724763f5f487bc0ded4dffd94a2163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:962d9491ef45aab5e15d9501a8aea3a22b239d68344325c3cb9cc318007a4d3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da344cce2a72ab4af56e7a14662833f72677bed0ef2fa896ee580e8e6573dec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:26 GMT
ADD file:54d60144d251caa916ff50606bc2364131d47d6b10ed83d08c81c647ab56cc40 in / 
# Wed, 11 May 2022 01:20:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:20:29 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b03a94565ecb6e02edf716307f25a0ea5090e3e2f7acec6a3687b95415378a30`  
		Last Modified: Wed, 11 May 2022 01:25:33 GMT  
		Size: 50.4 MB (50437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721d47c2a1c65734cd79baac75a8848c4e787e4aed18e13f24597f8407c500c8`  
		Last Modified: Wed, 11 May 2022 01:25:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d32d71f5cad53a976f4d108dd7103cc4ee7825880a244f03bb37ec7da9c64c46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48157744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8edddf8aefa7d078f3936f603e8616512bc0bf194bbd3680a6df0147f33ae92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:51:01 GMT
ADD file:8292d961a3aa3c4584c010be23306dbea6f52d4f69fe30d2b3ae6d2f8cb91f98 in / 
# Wed, 11 May 2022 00:51:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:51:17 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c49f9a696043c9b0e9c645a07e1bd105d319cdcc2a580c36b676431549349006`  
		Last Modified: Wed, 11 May 2022 01:06:38 GMT  
		Size: 48.2 MB (48157520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c36708df647b567de646d508abe210994b759478b90c8f53c550d5323b8ffe`  
		Last Modified: Wed, 11 May 2022 01:06:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0c5158b602b67820a2d87c8d4cd562195600b2505e412eeea4ebb91d0a370b0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf6ccac2edd52bb3ad69f82dae77e9a4d8210c256d9aff1b9e2c9ec3ed5b0e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:18 GMT
ADD file:3c8ac0c219015f8fbf065e01216d362016d6068cb4e73ea6f0a56893c235a2a7 in / 
# Sat, 28 May 2022 01:00:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:00:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59fe0b97900eb1b641ad94d8d8f3bd9dbff0472e481c4c4c38f2372ef790900a`  
		Last Modified: Sat, 28 May 2022 01:16:20 GMT  
		Size: 45.9 MB (45915564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c2f763c440da2a4e9a0fda390a39cbc4cff2eec626742ca45e7d304e4b91e8`  
		Last Modified: Sat, 28 May 2022 01:16:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:17d60f7c9a8dad1e2ec28e0b9e4b9f5e765cce599ab0b0d3868589a7d32b2e06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d39a45273b60b45ca625d3836fb54fddc2c988eca0c3b2f8165ed1310a10bf0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2572b176e5f0663c289ac7d37fba29edf2388af7d3dd5922ac484b1dee10ac`  
		Last Modified: Sat, 28 May 2022 00:48:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:f97e411dc15dbdc3b1de345e5e884eaeb2096958644cf8719f59b550d5a3cad3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45559a375aee7ce69325197ba649afe437952061c54679f975355bc13dd74848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:45 GMT
ADD file:3995ccc1e3f12a1e3f28dd818223bdc5454a7651248bfb98fae7c14961c49bba in / 
# Sat, 28 May 2022 00:39:45 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:39:52 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:045913a916496008850e7e3b499b9acc93c72b4018eda833a11c562a6d8413b5`  
		Last Modified: Sat, 28 May 2022 00:47:08 GMT  
		Size: 51.2 MB (51204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8d51807f32497c5d46e99f72a30bbad0017e16f7f0e97bb5b1cb6f9925fe9`  
		Last Modified: Sat, 28 May 2022 00:47:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:532c7013cba2963df1a89b17111cb51e5ce5abe3bff2179d348d48d873364f14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49073992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b67eb1b7c995a531d8942a9322232256240faf3f59ec90f27170c9a275ebe98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:24:09 GMT
ADD file:8196bde1e8989094969bcfd079f2fceac263a32d24556ea55bb20a53b915b112 in / 
# Wed, 11 May 2022 02:24:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:24:25 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:737cd4f99975def8d1d06011f9f8adfb43e6149a232c24f0bcfac82bbb3d809c`  
		Last Modified: Wed, 11 May 2022 02:34:25 GMT  
		Size: 49.1 MB (49073768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdb555ba564203fa83b9a1e64062f2950a5e9303327f0ec3bc4406cea46e49d`  
		Last Modified: Wed, 11 May 2022 02:34:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ee384deda5a8b44b118df916e8e28b89521c1134f9d8ff90805494334505d289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54170420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4396bcbd475f94ad7d395537cfd336d2db437041f363a15580d0dece2586554`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:32:53 GMT
ADD file:73ff2a18e50b226a862b74c50f091d80ddcd29f404879c4937887c560fdf624d in / 
# Wed, 11 May 2022 01:33:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:33:18 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:88d357d3afb8b0de721a4298ddb31fe73077663376e53d241a3d5217080e1f73`  
		Last Modified: Wed, 11 May 2022 01:43:32 GMT  
		Size: 54.2 MB (54170196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a6b9b5c68e3dcf66164673902943880c5ab9e17a534f9f6b2a1c38a9d82c53`  
		Last Modified: Wed, 11 May 2022 01:43:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:a0feb520b7fe97ec7fb37014d91bc5358f86c948b4dfff3d2fc5221f287a0a7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ff90c7e3f98a473d92f2e8f79d42aab9b376053332cf4ea708a8c0b8a67a2e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:20 GMT
ADD file:65712051a170cb9d0b18d0085bc26171598119b8946fa55b5ee959661b48a5d2 in / 
# Sat, 28 May 2022 00:43:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:34 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:771d2d61f47933c8d05a5f7e35dcb16848a6225e7531db8e5971d528982538e9`  
		Last Modified: Sat, 28 May 2022 00:50:02 GMT  
		Size: 49.0 MB (49006810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a644fc1b893fb3851590745b6a1cf8d7297398ef7cbe4dbf3c9940d6b1c0ee5`  
		Last Modified: Sat, 28 May 2022 00:50:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
