## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:ec2b2962b409c4e4eb890238a620026e4c909794057fa072c02889bd54e90584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2451b4cdecff4016c9fb931fb7f6bc781250614e197b9e1a6287d29a76da19ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41489698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1862aa27caa57e5cf692ef266914035e35ae6667a8e93ac89b45ddadfa4d5539`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:47:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f87743a51ebd3c3339057ac4b3ec85dc6978d0b2810c7e52fbb67db0710e9b8c`  
		Last Modified: Tue, 04 Jul 2023 03:57:50 GMT  
		Size: 27.7 MB (27723058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d294972834df62fa5155c9ab227aa39a4ee9d4ff010b19bc7f855b772262f2d`  
		Last Modified: Tue, 04 Jul 2023 03:57:48 GMT  
		Size: 13.8 MB (13766640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5b114307fa87536ec11392334596fc7032cb25d612fa7d87f979834f4ee55ce1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37940783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c190de988d49e8e1fdbe5bf67cb67246aade085b976a9a21e57b3d2963cc3ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d9959b212abdc29a099893ec5eeb0a1e80508f22581d6b7e8d7ac257769bee7`  
		Last Modified: Fri, 16 Jun 2023 01:00:47 GMT  
		Size: 25.3 MB (25271336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a3ceae76fca68286fb64b3323157a721f2f88a43cd21f69b7a567704523771`  
		Last Modified: Fri, 16 Jun 2023 01:00:46 GMT  
		Size: 12.7 MB (12669447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c39c8df9209fb057d42e507d33a397c4eeb66a6ffe70ed74d22535da5298a1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40412045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8696c8456822956dd26c435b59c4fc910da5ba981ca88a905b29ea4e957fa4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:14 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:16 GMT
ADD file:3f4faed988a03b7d05aefe677906592aade4d2bae1ec3f7055c1f10744a38de0 in / 
# Wed, 07 Jun 2023 04:42:16 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62f0439e6eacbe88b3b071461591f644c013d55d1bb0ecba6442ac98c987966e`  
		Last Modified: Fri, 16 Jun 2023 02:36:15 GMT  
		Size: 27.1 MB (27075677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4f6ab448c591bc2009541723cb7648afc9648bd50663a7868f9adb99bbb00`  
		Last Modified: Fri, 16 Jun 2023 02:36:13 GMT  
		Size: 13.3 MB (13336368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c786079e321a4781ad23c1e10d14a1e94bb6cb120b3637f07e1762348e8ec80a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47810906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f166f3608de9c676cd08ef0d69e735d9a7292b430751b30b5e7b7fcc790195`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:add2cbebe3a583002ff52a300bd69d6b961b4a7735c4612e8030bd26ad555288`  
		Last Modified: Tue, 04 Jul 2023 04:45:56 GMT  
		Size: 32.0 MB (31951571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de6196fb1fff1ebdd9bca2afdccb736f7418000536393564f88be29d3b0c74`  
		Last Modified: Tue, 04 Jul 2023 04:45:52 GMT  
		Size: 15.9 MB (15859335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab4328d5274768f0608716426e9ce2c956ab90efefcd7848844538af0ee711d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40288440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7f91374a9f3ad829228f1446965b4ef2c6bb72199c4542b8f261641a8c60f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:36 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:36 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:38 GMT
ADD file:4e8ca8820de4a27d67ad223be645ce7a7a48289dfcbc01b4e1dbe3bc74ebbc56 in / 
# Wed, 07 Jun 2023 04:42:38 GMT
CMD ["/bin/bash"]
# Sat, 17 Jun 2023 09:56:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6943591795586ce983bdf25369a45a8d58f64cd04bb9b22a9ebfbbbcaa9443a`  
		Last Modified: Sat, 17 Jun 2023 10:03:01 GMT  
		Size: 26.3 MB (26281083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031ae27af25073c29d7050bd7d1de8c0178d4af4c165618364aec7a707620748`  
		Last Modified: Sat, 17 Jun 2023 10:02:59 GMT  
		Size: 14.0 MB (14007357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
