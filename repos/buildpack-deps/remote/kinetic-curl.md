## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:5f258549467fe3f0ff090cae8e793f4697af0cb53ad350bae8adb06e2d47e67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4a0ea70e27ab3ee9d260740e1e11ef06f009589299eaa372b3313a5d617480bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37888050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83a06332258b828506b4757d4fa816eb9f29440d4e56282a9a38e120f33cd5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:58:05 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:58:05 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:58:07 GMT
ADD file:3492508b382c909e968c4d8467b9acbd5f61ed6ca69c8a47241f930d90de7158 in / 
# Wed, 08 Mar 2023 05:58:07 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:33:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:33:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:17a407a0ba4a4df07961f83dc5f45a6167aef7c4f6ca31fb67cb40abd601132d`  
		Last Modified: Thu, 16 Mar 2023 05:44:13 GMT  
		Size: 27.5 MB (27482092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3ce1e417f7729d7a549758b735166f99e55a7991459164e9a2cdee45bf49a4`  
		Last Modified: Thu, 16 Mar 2023 05:44:09 GMT  
		Size: 6.8 MB (6770607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f86ef9e483dabe62f207ba172ab1901264fcb5d62bd81ef5221c8ce9d67b3`  
		Last Modified: Thu, 16 Mar 2023 05:44:09 GMT  
		Size: 3.6 MB (3635351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4af883c5eab3c2380a46236ca3ca95f3048243965b2e897814c48e8260dfa2c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35633477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d55cec9f8dc3d95b8ee21b11560284d162a4571f93b0b44109e9fe8e3d0cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:55:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:55:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:55:49 GMT
ADD file:827330b6c59e67c5d2edd3ceb3492b97865b15f9246f14710f478d12e94d2048 in / 
# Wed, 08 Mar 2023 05:55:49 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:56:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:56:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6408fcff70bde57e1c23e7502a9476939cc569e2eff3e9e9adca350cb5b4dac1`  
		Last Modified: Thu, 16 Mar 2023 04:10:41 GMT  
		Size: 25.9 MB (25890803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467248c617f5da80617561605e184647a03bc6ee0731094ea5fa1a10a9d97d12`  
		Last Modified: Thu, 16 Mar 2023 04:10:38 GMT  
		Size: 5.9 MB (5941308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed064758ff6efc72c5bfa16404dd5e5a7196c6704c9bfce54fffbe511f026`  
		Last Modified: Thu, 16 Mar 2023 04:10:37 GMT  
		Size: 3.8 MB (3801366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f7410e86839d94189da0421368263daad23e4532602532ebebb243959a6589bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36907970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11201af935ca582771cd9c1d5a25562f6956d2d83b5561f776ff20235996f3a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:57:57 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:57:58 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:57:59 GMT
ADD file:884e00dc91bf6d392fa3d117913cc2534177128322d89137bfb8b2734bc38579 in / 
# Wed, 08 Mar 2023 05:58:00 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:12:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:254a784e837e29e485a63351d1a7aba22a34cad2c55e16264bd25ec0add89463`  
		Last Modified: Thu, 16 Mar 2023 04:24:12 GMT  
		Size: 26.7 MB (26703428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c5262eba6308f5bd6759d8fe45a1d30f1c39e36af3ffc10b11c84e335e3cf5`  
		Last Modified: Thu, 16 Mar 2023 04:24:10 GMT  
		Size: 6.6 MB (6600337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d93a07df4f2da69d3c85f944e8fa42f4e401cfb09edbff605d5863469a8c37`  
		Last Modified: Thu, 16 Mar 2023 04:24:09 GMT  
		Size: 3.6 MB (3604205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a173db92e12ea4bc7ab8861dc75b1d01163b4169bf587bcbdf056ceceef84f9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa7da5a02e3ed5cc84aef25afdec00f9462f210848b3903b605466dcbf679da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9a30abdb96a71c9bfe40e06305587f2453f48e6826253c2346f68c867918c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36122431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d179c68254fd9641c116296236caf4426c7b9a75a4eef7ff30749528c41b419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
