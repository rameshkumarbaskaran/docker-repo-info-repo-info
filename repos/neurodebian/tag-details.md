<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:2429604df643c021ff2cab3dac991a0fa74772bf0b83861bd2ecd784fe0da05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:ada092c3a0c585f13d5f793e7205070600af63e45981298386e2dababa1d738a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97eecada419163ee3c517ac6705ef6e5dfa59771e40d23b94dfc828b9d1d62c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a4b5dc9653f9c297b655b999a18dc419aa1de140d5f0922e669d63ba8f81e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d4d01492647633a3360a913f3e312b6b59ea3c99348fb6c59efd5147552260`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:088603ff4edc4022b00300092617e96a8049eeb012b4171c88cb69e1deaed5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9e8ffa5a31ecac0fc53ac08f758b6f3acd6aa33812e5f0d0527472b9b881dfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bb7a8f0e8135403e8e485b1e329938addf81ddadf3098c440a8e59666b9b66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da88f82f719637c6eaba4b8175eda88b088da7adfc3952ff2732a42ed676775e`  
		Last Modified: Thu, 16 Mar 2023 05:58:04 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f9f953e47a67b48292e1ce793d31c3c7189d274b938ad5449b46e116d25a8a6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072b8fb76cb79a0ce80d413e95024a3f0fc969a9404af11cc642f6fc269db7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505f3caedc8772916ffde5305b38400b1745044ad55838322de25760fb04dc4a`  
		Last Modified: Thu, 16 Mar 2023 02:42:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:eaa0265ef8a83c7230b132b2d7d6efd363ae31d615303003b3093463cabe3847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:932bb55767f864483dabf659bc1478657d9687caa790b3ec66823985442094b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61221640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaaea80b89361d286ce1a5f78f241b6db808d8ba562e20e6b71d72e7c1a8150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52994b17c4fe57d87d958eb629cb4e4209d0970f24f33d1fc9b7d345b09becc6`  
		Last Modified: Wed, 01 Mar 2023 16:46:41 GMT  
		Size: 11.7 MB (11701029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b6d88a3f003e541f63f77bbfef90ff8da9913559b8f6936040ce19f1054f6`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe2174f024898bc0d4770401ad4c9b4aea1bae0037db73bd30859bcb386613`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7d6227c840a491568c618da76c10e8e0b3f3d5d4174612c084763b90e8cdf`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 281.3 KB (281327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dbc36b82a1cd241cb7bc26f648432524ded15a211d3a43bf21a7afd3e4671dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61218749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87132c851b3adcb16e0de665de571504e31dd1925102fa584944ff7096acd46a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e5113fd09171ab576c1d16b344acf0e917e04d98112db25425b0d5728ea300e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557d46a191412276903630954b271d01ce46d04c01a44e474ff3e6e2c21a8419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:3f540f3651847265b086d9c3801109dfe13987011171da20df01e5c7bca43bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b02cb24b04b44a44f2ed39d4efb47e49e8e18df5b7be43bd623ee3560f80faba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61222069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f96d2825762e3c4d76c0340e16f7abb00175734304f5ae394c7f90301829ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52994b17c4fe57d87d958eb629cb4e4209d0970f24f33d1fc9b7d345b09becc6`  
		Last Modified: Wed, 01 Mar 2023 16:46:41 GMT  
		Size: 11.7 MB (11701029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b6d88a3f003e541f63f77bbfef90ff8da9913559b8f6936040ce19f1054f6`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe2174f024898bc0d4770401ad4c9b4aea1bae0037db73bd30859bcb386613`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7d6227c840a491568c618da76c10e8e0b3f3d5d4174612c084763b90e8cdf`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 281.3 KB (281327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7491030f693c1cc4b1eea96acb7ae2560e0975e7eaa1e6129035f143dccd091e`  
		Last Modified: Wed, 01 Mar 2023 16:46:48 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e7370003f0ed9dec23acc7f29b0815ab397afd432b2df18e599b9b102e89775e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61219181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7c0832f70f46788003d977bea0b614e36cf4bfcc2cc3adc779aa0e040d55ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfbe0c4ee6dacde7a5bf899793444841c5a20f08af294bad3a3a88be2ef2be9`  
		Last Modified: Wed, 01 Mar 2023 05:02:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f5fb222c99bb60ec1873ec12109f2100cc2f7c0c0c4c49ebb862931a40cdd778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09e3e4c39734921aa13a5fdf12088049ecffc7f768a939e9d66a1f34b502ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81dfd8e9fbdde88d17ac8708e298dfcd7fdad09eda77db2790d4525ee1b50c3`  
		Last Modified: Wed, 01 Mar 2023 14:04:58 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:a12cde1cbf1b83810856d89f09120dd08b25074c20eb542b600ea071e49e9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:b83d8691ba15eac0b02d0638d4a3a0adeb005c24cc45010766f5bf7ff1577101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95abf467c26b3ba6e879ffe6dbbb01f9f1f7feb6fde75c2a75eabd86461b4908`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:811c80f3740526e4c03bb62afa7850d4860643911f7e8ca2dbad624961b27236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd71c1e2e15f6ecdff570d00470791ba487f059a952d5fe91e6f0d5688c86e29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:be1492b0401753ac150dfa176689b9f9197e2555a1c0358626bde3c061ed4d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:397850dd721f2d70f2666b6034e38902616f1811810b36c57856e53a045e9260
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570f9463ec5d93718c4ef20e1a5a0bb21677e80bc18d56c0e717c38e26c8b4c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a90083e3034d3bc1b9cd93ac980645679a1506f873cd25e8759b770d6a61461`  
		Last Modified: Wed, 01 Mar 2023 16:46:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eeeb799d1653042b93fdcd8ddddf38f470636f27f9bfbd8ee44094494d5bd035
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea6141601a32ef3e9ddb787af10b16777d10e6f802f5ea43b2e1ad73737a2db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759b54753a4731feb4431d567233efa66a2581b07b96efd4dda8f8525a0ee65`  
		Last Modified: Wed, 01 Mar 2023 05:02:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:af9273acf81c0273b30a873be2cd2a7600b1217ecd627ef705d56b203be9c876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:bbddc17c272867a26b7feed992e6ecbff77530ab31f1ccf164387e2e011713eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83519bdaca7698b3e1ac7c03a156250b231ffd570ab3b8b38b0c735167658d1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612b2f2d9c74944c483a61ee943e6a24b2007abb878645afa5615ecc0df4c2`  
		Last Modified: Wed, 01 Mar 2023 16:46:00 GMT  
		Size: 10.5 MB (10504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22335a31d3b76cdfa76c4395a76ff316493877e2615246522b95b9d6a9e354f`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f271e3ec83792f994560a4c28bca958e6e8a218dbafde7ca87a9ecab9d5a8f51`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740ee30f013b293d5925c48e7a80c75a12a7aa8347301b39ce884e8f2c3203d`  
		Last Modified: Wed, 01 Mar 2023 16:45:59 GMT  
		Size: 304.3 KB (304342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1525d4f614299a5919d27db99ae1fdf626b2ed793f96c9450bd6befb7156d933
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0821d4fb1e7367429fb9847b9f6255fa3da21060eff616acda475e7275f9e48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f17a319adfdaf70a0743c908ed30a76d664f69e943708f0373c6da2c9c67b7`  
		Last Modified: Wed, 01 Mar 2023 05:02:02 GMT  
		Size: 10.5 MB (10510356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb398b76429a8b2432811dfcbcb6348bb36b23bd016af5d310d19c8c445d64`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf77cd6bf30274d4a68a065b517df02742ff5dba187db54ee967c6fc4210736d`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea7526c13547805ba46a2fef0ad342e282d2fb5726b30dc02c59c32bcebe7b`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 304.3 KB (304317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:96124b0d939cd9453d1f5bd48eaf28f9604b813af5f93a0ee05a6e5e9843f7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513b02edc7b5e1bfa4491c5259504ada968aaf72d7088609818f6f63a6d4e73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:dd95fd0af5bffbd527a97b6bf3548a6652df26e0447ead3cf9431eeb53dd1146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:796e97071137a7a1d9ddc4fafbed997b1fc1f52d5181db7c54f78943300a9d42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6190558bdd0952faddf9c19bc813b07f767e3d22a527f9f602506712cec7372`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612b2f2d9c74944c483a61ee943e6a24b2007abb878645afa5615ecc0df4c2`  
		Last Modified: Wed, 01 Mar 2023 16:46:00 GMT  
		Size: 10.5 MB (10504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22335a31d3b76cdfa76c4395a76ff316493877e2615246522b95b9d6a9e354f`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f271e3ec83792f994560a4c28bca958e6e8a218dbafde7ca87a9ecab9d5a8f51`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740ee30f013b293d5925c48e7a80c75a12a7aa8347301b39ce884e8f2c3203d`  
		Last Modified: Wed, 01 Mar 2023 16:45:59 GMT  
		Size: 304.3 KB (304342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abf1caab23b69d23e2ba286f966108244147ffa2bb4321536402b0189f4227f`  
		Last Modified: Wed, 01 Mar 2023 16:46:09 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0d1d6eb19e18f6ac3d05f9e596e9830b7b478648e6cac296112c1ef9bfbbb7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60057040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd60cdda08423f59d6bd5a001400c73153e5d6a40a37837cb7d2771936674f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f17a319adfdaf70a0743c908ed30a76d664f69e943708f0373c6da2c9c67b7`  
		Last Modified: Wed, 01 Mar 2023 05:02:02 GMT  
		Size: 10.5 MB (10510356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb398b76429a8b2432811dfcbcb6348bb36b23bd016af5d310d19c8c445d64`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf77cd6bf30274d4a68a065b517df02742ff5dba187db54ee967c6fc4210736d`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea7526c13547805ba46a2fef0ad342e282d2fb5726b30dc02c59c32bcebe7b`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 304.3 KB (304317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3545fb879d6379e51745374d6f1d63a7ae2126141a15b12572b6355ded4d8f69`  
		Last Modified: Wed, 01 Mar 2023 05:02:11 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3317c07eda65fb456e1fb7372dcf45379845b3fabd59aaf6cb390fabed893fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32adb5752d709797e0414a4d9b854663dcd211fd8f990390d1a6356b2cbd7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a7ebbf20b05aa1bc459f99a4e5299be2866f5a1f1c10119f96e417677ce6f9`  
		Last Modified: Wed, 01 Mar 2023 14:04:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:cf735919f0a9cc5aea3daf7ab80d7f93ad8ca2afba62bb55c07f2a0bcefa9780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a99108bea9d07e5335225edd6ed83221e8408f2f0ea1c91a9bb60567127f65d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff0277e3ae878c0028f0d36cd89f9a1e74128f131914a395ce680396e7e671`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da7229782d5fba3c8438c2b2de88bd3c6099ae476b1703fa26e86395a7562083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563d61ed1e782e4a6aaa7a5d76b241ebd72621b74a11f862ab60ded47aa82b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:1b211a877b07ea4e1af7555214e58aeb850488ae2bca0bdd37c08ed013fe615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc97612a4116bab9949b583fb9c895b6a057a55ff0eb6fd8272d87a1d152cbea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d48b1adf7bba169d225b2bd8b8edcb1ad2c286e8ca68520b5174d3a18b7d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf30130b0e476fe071e98d9ab2c3175b52a7508cb1e62517a27f3e948ca612`  
		Last Modified: Thu, 16 Mar 2023 05:58:21 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:546a886a46534eb07c9d82a7390048541674fc3b5d15c1d5905dbdb9a3263de5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f67aad37e1f08a1df26e7dc3fbeeec841d3e9dd70921d5dc3d40493fa9dd07c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61d991a58959ac33992a13de9a8889e155ffb794facc83d7bd5d7727080bc7`  
		Last Modified: Thu, 16 Mar 2023 02:43:10 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:43553d3ebc3be2e84e9750c76af18f59fcc1cae78f4d4886fdaa6b3bda22a8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:73c2f226b9d41a6ca475169b8a89e70fc0d8a921923c02d8afcb664afd8d8f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7191d88ea89379c7d8e2774cec92200333c8a7c2f3451a3cc48413f526dee25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c95488ad407602f3428cc2f1ca2a18fae5d6a574d08748cb496395700cf21a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db42a4a163de92fa05e1a55401762179cf3d028caf4e35c98f0f3914c62b0448`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:befaa46361e4cdf5e51af9449a8b44252a0de82fcffdfc01ec72fa2dca2db88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:52c45e356c8aa65f0195280d10137325b7079ffdaa1d264f97c21d6af24e6078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c7a0db011b4f391a443a7124397742ff9157869a66ae55e6e7f191966c5ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:57:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab5940b1d2c038782f17a50acc9126268be50075871c55afb2186fbc68e4bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4ac76a3c541cd78be3cddc5ff62f5665c6431aba800889e736786318e40285e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f25d7769d9cd3afa3b69a5e1309559b4abf92742d07f0f98b6f70396fb197`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338595f61a4f73430e7935e55fd6a4e9ed2ab7cab265310c9c90f41b00b94686`  
		Last Modified: Thu, 16 Mar 2023 02:43:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:a12cde1cbf1b83810856d89f09120dd08b25074c20eb542b600ea071e49e9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:b83d8691ba15eac0b02d0638d4a3a0adeb005c24cc45010766f5bf7ff1577101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95abf467c26b3ba6e879ffe6dbbb01f9f1f7feb6fde75c2a75eabd86461b4908`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:811c80f3740526e4c03bb62afa7850d4860643911f7e8ca2dbad624961b27236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd71c1e2e15f6ecdff570d00470791ba487f059a952d5fe91e6f0d5688c86e29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:c99a320f5b489b4b9fd685aa70c861a8e77a3129f3bb1c530d0922b327c88221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0ffafd9fe3daf7efd5f712fc3d053b225086b1827a78e47db5a7431e4be36f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdf78211984955858995b9d812f932ac9d4b78d162415e9b8f88e9d3cb9507`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b922cad3fe5d3b4160ae7b3a5e81a57639a85513db1e474d1ec0eef9c6590bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d236ae8b1b48090ac45a3c137236d2519bd66c888ac05b2259490ed82bab035a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:01:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c660fc12919553d4c7aa5bc89004fe56e8844231dce893e94984fe56dc23`  
		Last Modified: Wed, 01 Mar 2023 05:03:00 GMT  
		Size: 11.7 MB (11661138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19c97c2997b743d321faeb9616b3a6e870b9fce608c572197aeab2f394c594`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9217cf8b3cf849d5480f0b028fe5a6a95663fa518c91e44ada3d8c7e086baf`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a238e1cc1f54ddef9247ec8bf508b59a49995e1564a673f8947751096ea9f5`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 282.2 KB (282223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:f528b19cc612f1d1444e5a4e3a3acf883bfca110b57d86b7f6f1e244c844f371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62722827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5387b36ce2af622c1e0eba8fe0b4347ccf401180723bdcb1bd9eee565933a3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:b2d0ed22177b3c3c8cb5d6d6a25905af2773c600258c137a9793979a87c1ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:afa4b10de84e23db29f6f1b7d6ef28195645f359c8bd6a4e0262ddb6fcc5a597
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f356db77ba481cb1de7195e9ed0a895d3b289dde5a5d61a99dcba2b2c8b33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06941c2c76256cec7bbde5b3f998444239e34aa3cfd46afe763196c5dcba4b36`  
		Last Modified: Wed, 01 Mar 2023 16:47:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9fc9ba0c241d8f9728643ff32c6917a453ccbc5c41dabcd51275bf322a03d2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476fcee5f96b3a7ad70dee55321deb7000b054866b61a10148784d9f7d2f4d52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:01:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c660fc12919553d4c7aa5bc89004fe56e8844231dce893e94984fe56dc23`  
		Last Modified: Wed, 01 Mar 2023 05:03:00 GMT  
		Size: 11.7 MB (11661138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19c97c2997b743d321faeb9616b3a6e870b9fce608c572197aeab2f394c594`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9217cf8b3cf849d5480f0b028fe5a6a95663fa518c91e44ada3d8c7e086baf`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a238e1cc1f54ddef9247ec8bf508b59a49995e1564a673f8947751096ea9f5`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 282.2 KB (282223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9240d83d2e30f2e3699c4bc43a52d90ccd538a47c8632e6b90692688dfff0af4`  
		Last Modified: Wed, 01 Mar 2023 05:03:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf1388217fc75201eec1764ecf9ccc9d84becbc1a5c2fff97de123176d113bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5280e2b5efae98def7467cf9eecfc70f505f631e134aee484003dfdb9202f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61643c2ab05c90ffcc0f8e261d002b4cd8d654267ceadef7f14d5b5f46a05348`  
		Last Modified: Wed, 01 Mar 2023 14:25:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:af9273acf81c0273b30a873be2cd2a7600b1217ecd627ef705d56b203be9c876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:bbddc17c272867a26b7feed992e6ecbff77530ab31f1ccf164387e2e011713eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83519bdaca7698b3e1ac7c03a156250b231ffd570ab3b8b38b0c735167658d1d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612b2f2d9c74944c483a61ee943e6a24b2007abb878645afa5615ecc0df4c2`  
		Last Modified: Wed, 01 Mar 2023 16:46:00 GMT  
		Size: 10.5 MB (10504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22335a31d3b76cdfa76c4395a76ff316493877e2615246522b95b9d6a9e354f`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f271e3ec83792f994560a4c28bca958e6e8a218dbafde7ca87a9ecab9d5a8f51`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740ee30f013b293d5925c48e7a80c75a12a7aa8347301b39ce884e8f2c3203d`  
		Last Modified: Wed, 01 Mar 2023 16:45:59 GMT  
		Size: 304.3 KB (304342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1525d4f614299a5919d27db99ae1fdf626b2ed793f96c9450bd6befb7156d933
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0821d4fb1e7367429fb9847b9f6255fa3da21060eff616acda475e7275f9e48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f17a319adfdaf70a0743c908ed30a76d664f69e943708f0373c6da2c9c67b7`  
		Last Modified: Wed, 01 Mar 2023 05:02:02 GMT  
		Size: 10.5 MB (10510356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb398b76429a8b2432811dfcbcb6348bb36b23bd016af5d310d19c8c445d64`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf77cd6bf30274d4a68a065b517df02742ff5dba187db54ee967c6fc4210736d`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea7526c13547805ba46a2fef0ad342e282d2fb5726b30dc02c59c32bcebe7b`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 304.3 KB (304317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:96124b0d939cd9453d1f5bd48eaf28f9604b813af5f93a0ee05a6e5e9843f7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513b02edc7b5e1bfa4491c5259504ada968aaf72d7088609818f6f63a6d4e73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:dd95fd0af5bffbd527a97b6bf3548a6652df26e0447ead3cf9431eeb53dd1146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:796e97071137a7a1d9ddc4fafbed997b1fc1f52d5181db7c54f78943300a9d42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6190558bdd0952faddf9c19bc813b07f767e3d22a527f9f602506712cec7372`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f612b2f2d9c74944c483a61ee943e6a24b2007abb878645afa5615ecc0df4c2`  
		Last Modified: Wed, 01 Mar 2023 16:46:00 GMT  
		Size: 10.5 MB (10504458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22335a31d3b76cdfa76c4395a76ff316493877e2615246522b95b9d6a9e354f`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f271e3ec83792f994560a4c28bca958e6e8a218dbafde7ca87a9ecab9d5a8f51`  
		Last Modified: Wed, 01 Mar 2023 16:45:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740ee30f013b293d5925c48e7a80c75a12a7aa8347301b39ce884e8f2c3203d`  
		Last Modified: Wed, 01 Mar 2023 16:45:59 GMT  
		Size: 304.3 KB (304342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abf1caab23b69d23e2ba286f966108244147ffa2bb4321536402b0189f4227f`  
		Last Modified: Wed, 01 Mar 2023 16:46:09 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0d1d6eb19e18f6ac3d05f9e596e9830b7b478648e6cac296112c1ef9bfbbb7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60057040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd60cdda08423f59d6bd5a001400c73153e5d6a40a37837cb7d2771936674f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f17a319adfdaf70a0743c908ed30a76d664f69e943708f0373c6da2c9c67b7`  
		Last Modified: Wed, 01 Mar 2023 05:02:02 GMT  
		Size: 10.5 MB (10510356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb398b76429a8b2432811dfcbcb6348bb36b23bd016af5d310d19c8c445d64`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf77cd6bf30274d4a68a065b517df02742ff5dba187db54ee967c6fc4210736d`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea7526c13547805ba46a2fef0ad342e282d2fb5726b30dc02c59c32bcebe7b`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 304.3 KB (304317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3545fb879d6379e51745374d6f1d63a7ae2126141a15b12572b6355ded4d8f69`  
		Last Modified: Wed, 01 Mar 2023 05:02:11 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3317c07eda65fb456e1fb7372dcf45379845b3fabd59aaf6cb390fabed893fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62382364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32adb5752d709797e0414a4d9b854663dcd211fd8f990390d1a6356b2cbd7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:01:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:01:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:01:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da67baad9b0f9e7bc5adc526954637e4319038c09fb5b88d95602ebb082643f2`  
		Last Modified: Wed, 01 Mar 2023 14:04:03 GMT  
		Size: 10.9 MB (10868322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d9fb5f6e1a0497e5e5bce467eda0a0f642506ee3d02e91fb20ecaf850021e`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f20e5d63d935ba225224f7bd32c62b1fde78f1360d8abba264bb6931fd478`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1207f0083a5fba06d163124bc9a5637daf92d4d3bdfc83385a36dce0e78244`  
		Last Modified: Wed, 01 Mar 2023 14:04:01 GMT  
		Size: 304.3 KB (304281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a7ebbf20b05aa1bc459f99a4e5299be2866f5a1f1c10119f96e417677ce6f9`  
		Last Modified: Wed, 01 Mar 2023 14:04:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:a12cde1cbf1b83810856d89f09120dd08b25074c20eb542b600ea071e49e9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:b83d8691ba15eac0b02d0638d4a3a0adeb005c24cc45010766f5bf7ff1577101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95abf467c26b3ba6e879ffe6dbbb01f9f1f7feb6fde75c2a75eabd86461b4908`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:811c80f3740526e4c03bb62afa7850d4860643911f7e8ca2dbad624961b27236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd71c1e2e15f6ecdff570d00470791ba487f059a952d5fe91e6f0d5688c86e29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:be1492b0401753ac150dfa176689b9f9197e2555a1c0358626bde3c061ed4d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:397850dd721f2d70f2666b6034e38902616f1811810b36c57856e53a045e9260
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570f9463ec5d93718c4ef20e1a5a0bb21677e80bc18d56c0e717c38e26c8b4c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a90083e3034d3bc1b9cd93ac980645679a1506f873cd25e8759b770d6a61461`  
		Last Modified: Wed, 01 Mar 2023 16:46:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eeeb799d1653042b93fdcd8ddddf38f470636f27f9bfbd8ee44094494d5bd035
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea6141601a32ef3e9ddb787af10b16777d10e6f802f5ea43b2e1ad73737a2db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759b54753a4731feb4431d567233efa66a2581b07b96efd4dda8f8525a0ee65`  
		Last Modified: Wed, 01 Mar 2023 05:02:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:eaa0265ef8a83c7230b132b2d7d6efd363ae31d615303003b3093463cabe3847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:932bb55767f864483dabf659bc1478657d9687caa790b3ec66823985442094b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61221640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaaea80b89361d286ce1a5f78f241b6db808d8ba562e20e6b71d72e7c1a8150`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52994b17c4fe57d87d958eb629cb4e4209d0970f24f33d1fc9b7d345b09becc6`  
		Last Modified: Wed, 01 Mar 2023 16:46:41 GMT  
		Size: 11.7 MB (11701029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b6d88a3f003e541f63f77bbfef90ff8da9913559b8f6936040ce19f1054f6`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe2174f024898bc0d4770401ad4c9b4aea1bae0037db73bd30859bcb386613`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7d6227c840a491568c618da76c10e8e0b3f3d5d4174612c084763b90e8cdf`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 281.3 KB (281327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dbc36b82a1cd241cb7bc26f648432524ded15a211d3a43bf21a7afd3e4671dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61218749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87132c851b3adcb16e0de665de571504e31dd1925102fa584944ff7096acd46a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:e5113fd09171ab576c1d16b344acf0e917e04d98112db25425b0d5728ea300e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557d46a191412276903630954b271d01ce46d04c01a44e474ff3e6e2c21a8419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:3f540f3651847265b086d9c3801109dfe13987011171da20df01e5c7bca43bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b02cb24b04b44a44f2ed39d4efb47e49e8e18df5b7be43bd623ee3560f80faba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61222069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f96d2825762e3c4d76c0340e16f7abb00175734304f5ae394c7f90301829ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:21 GMT
ADD file:74b4e0fbcb9cb38344c32a0512a72d8179f885de4b7bb127215f8d96a6262664 in / 
# Wed, 01 Mar 2023 04:09:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9d915a4248d2913bb8451eba978ac348a983990eca9186543367f5f44900e0fb`  
		Last Modified: Wed, 01 Mar 2023 04:13:25 GMT  
		Size: 49.2 MB (49237273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52994b17c4fe57d87d958eb629cb4e4209d0970f24f33d1fc9b7d345b09becc6`  
		Last Modified: Wed, 01 Mar 2023 16:46:41 GMT  
		Size: 11.7 MB (11701029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b6d88a3f003e541f63f77bbfef90ff8da9913559b8f6936040ce19f1054f6`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe2174f024898bc0d4770401ad4c9b4aea1bae0037db73bd30859bcb386613`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af7d6227c840a491568c618da76c10e8e0b3f3d5d4174612c084763b90e8cdf`  
		Last Modified: Wed, 01 Mar 2023 16:46:39 GMT  
		Size: 281.3 KB (281327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7491030f693c1cc4b1eea96acb7ae2560e0975e7eaa1e6129035f143dccd091e`  
		Last Modified: Wed, 01 Mar 2023 16:46:48 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e7370003f0ed9dec23acc7f29b0815ab397afd432b2df18e599b9b102e89775e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61219181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7c0832f70f46788003d977bea0b614e36cf4bfcc2cc3adc779aa0e040d55ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfbe0c4ee6dacde7a5bf899793444841c5a20f08af294bad3a3a88be2ef2be9`  
		Last Modified: Wed, 01 Mar 2023 05:02:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f5fb222c99bb60ec1873ec12109f2100cc2f7c0c0c4c49ebb862931a40cdd778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62682622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f09e3e4c39734921aa13a5fdf12088049ecffc7f768a939e9d66a1f34b502ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:40 GMT
ADD file:0ccdbb7b1f104c23abcf77c506eed771d5759d210c2284a95f85e558405a5390 in / 
# Wed, 01 Mar 2023 01:38:40 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b5ba6d7d02dd42cc6291ae5b4e129956756f664662a78db71f320107a1b6d189`  
		Last Modified: Wed, 01 Mar 2023 01:43:30 GMT  
		Size: 50.3 MB (50273396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95ed42da246160743d4dc3cd48dce0a186520ce89939f62fa3816eea4269790`  
		Last Modified: Wed, 01 Mar 2023 14:04:49 GMT  
		Size: 12.1 MB (12125266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543db8bb07019add3d3b7dc751cfde9eb3b093bb895d849804ac7dcfd952383`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778c4d44308786afcaf59829583bb93d4db04bba362c9b4c6759fb0a9602e06`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4758461e36efc6a403fd95256a5fefc7161101d33b99ae9d6a109a2c2bbbc`  
		Last Modified: Wed, 01 Mar 2023 14:04:47 GMT  
		Size: 281.5 KB (281517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81dfd8e9fbdde88d17ac8708e298dfcd7fdad09eda77db2790d4525ee1b50c3`  
		Last Modified: Wed, 01 Mar 2023 14:04:58 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:2429604df643c021ff2cab3dac991a0fa74772bf0b83861bd2ecd784fe0da05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ada092c3a0c585f13d5f793e7205070600af63e45981298386e2dababa1d738a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97eecada419163ee3c517ac6705ef6e5dfa59771e40d23b94dfc828b9d1d62c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a4b5dc9653f9c297b655b999a18dc419aa1de140d5f0922e669d63ba8f81e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d4d01492647633a3360a913f3e312b6b59ea3c99348fb6c59efd5147552260`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:088603ff4edc4022b00300092617e96a8049eeb012b4171c88cb69e1deaed5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9e8ffa5a31ecac0fc53ac08f758b6f3acd6aa33812e5f0d0527472b9b881dfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bb7a8f0e8135403e8e485b1e329938addf81ddadf3098c440a8e59666b9b66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d557fe244aea36536f8182abeb80171edca6a95656ec51733c3216706890ce`  
		Last Modified: Thu, 16 Mar 2023 05:57:56 GMT  
		Size: 4.8 MB (4821313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222fc36027e11ff005c44b53198ae32860241a12107c2b7516a055861d9d469`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818616c9c2a73168dd71f5a345a9d7fd898a01ed38687cc4abdfccf1327de03`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61af11b5775fb47759206cc8eefbae0ae400ead2d970643249809f8bd077e417`  
		Last Modified: Thu, 16 Mar 2023 05:57:55 GMT  
		Size: 240.4 KB (240432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da88f82f719637c6eaba4b8175eda88b088da7adfc3952ff2732a42ed676775e`  
		Last Modified: Thu, 16 Mar 2023 05:58:04 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f9f953e47a67b48292e1ce793d31c3c7189d274b938ad5449b46e116d25a8a6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28381792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072b8fb76cb79a0ce80d413e95024a3f0fc969a9404af11cc642f6fc269db7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b879e8702247c63c0da8736eb9b1565154a1ff5c5d5b358a3329ec11a18873d`  
		Last Modified: Thu, 16 Mar 2023 02:42:45 GMT  
		Size: 4.4 MB (4403813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000522275161a4c927a19ac80d50a7df6b4b777e6498219122d43443fc3f9c15`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e594af01efb4d25989d0c29d27ec67d513cbd1491df63e3480a80e6f082069c`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc185abdf3c8e1532c54a506d061143aea6e19bce06379477487dbeec9d63751`  
		Last Modified: Thu, 16 Mar 2023 02:42:44 GMT  
		Size: 241.1 KB (241110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505f3caedc8772916ffde5305b38400b1745044ad55838322de25760fb04dc4a`  
		Last Modified: Thu, 16 Mar 2023 02:42:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:cf735919f0a9cc5aea3daf7ab80d7f93ad8ca2afba62bb55c07f2a0bcefa9780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:a99108bea9d07e5335225edd6ed83221e8408f2f0ea1c91a9bb60567127f65d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff0277e3ae878c0028f0d36cd89f9a1e74128f131914a395ce680396e7e671`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da7229782d5fba3c8438c2b2de88bd3c6099ae476b1703fa26e86395a7562083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563d61ed1e782e4a6aaa7a5d76b241ebd72621b74a11f862ab60ded47aa82b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:1b211a877b07ea4e1af7555214e58aeb850488ae2bca0bdd37c08ed013fe615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc97612a4116bab9949b583fb9c895b6a057a55ff0eb6fd8272d87a1d152cbea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d48b1adf7bba169d225b2bd8b8edcb1ad2c286e8ca68520b5174d3a18b7d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9cbede0a5f1bfcbc8e1cd707920f95860c01ffe2181c4337499633f7ed1b3`  
		Last Modified: Thu, 16 Mar 2023 05:58:13 GMT  
		Size: 5.5 MB (5494298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d289892be04798f83785820b67592fe2408f79248ce26bad66abf4b4907bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e45c0dc53c16a4874bcb0da58df4565d01d1089508ceb6bce57d12166150dfe`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cdbf33fdf6703b4ef26d5b5ae6dae7e289c28fa214cde59803533689b6086c`  
		Last Modified: Thu, 16 Mar 2023 05:58:12 GMT  
		Size: 238.9 KB (238853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bf30130b0e476fe071e98d9ab2c3175b52a7508cb1e62517a27f3e948ca612`  
		Last Modified: Thu, 16 Mar 2023 05:58:21 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:546a886a46534eb07c9d82a7390048541674fc3b5d15c1d5905dbdb9a3263de5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f67aad37e1f08a1df26e7dc3fbeeec841d3e9dd70921d5dc3d40493fa9dd07c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61d991a58959ac33992a13de9a8889e155ffb794facc83d7bd5d7727080bc7`  
		Last Modified: Thu, 16 Mar 2023 02:43:10 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:43553d3ebc3be2e84e9750c76af18f59fcc1cae78f4d4886fdaa6b3bda22a8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:73c2f226b9d41a6ca475169b8a89e70fc0d8a921923c02d8afcb664afd8d8f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7191d88ea89379c7d8e2774cec92200333c8a7c2f3451a3cc48413f526dee25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c95488ad407602f3428cc2f1ca2a18fae5d6a574d08748cb496395700cf21a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db42a4a163de92fa05e1a55401762179cf3d028caf4e35c98f0f3914c62b0448`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:befaa46361e4cdf5e51af9449a8b44252a0de82fcffdfc01ec72fa2dca2db88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:52c45e356c8aa65f0195280d10137325b7079ffdaa1d264f97c21d6af24e6078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34456690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c7a0db011b4f391a443a7124397742ff9157869a66ae55e6e7f191966c5ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:56:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:56:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 05:56:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 05:57:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:57:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335e51c1d79876995a794864582f0195bc4a04de9ff98088f0f7c5232b2435b`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 3.8 MB (3765965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34419522da38584357ca1ca4d6aec0c6fb33a8304f58dd7bf0472465bd680be`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53390f3f0bfad1eb79041a646cf477888ffc151b4268f764bc07391c2bf6301`  
		Last Modified: Thu, 16 Mar 2023 05:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d191dd39f5b3c8ea8d1d854cfa38a556b55386315445df632dba15a405da6c`  
		Last Modified: Thu, 16 Mar 2023 05:58:29 GMT  
		Size: 258.5 KB (258490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab5940b1d2c038782f17a50acc9126268be50075871c55afb2186fbc68e4bc`  
		Last Modified: Thu, 16 Mar 2023 05:58:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4ac76a3c541cd78be3cddc5ff62f5665c6431aba800889e736786318e40285e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f25d7769d9cd3afa3b69a5e1309559b4abf92742d07f0f98b6f70396fb197`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c210859096ec9a9dfd6f1ecd0ee37c4daefba3d4025a0d6bc24cc10918d5b01`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 3.7 MB (3738163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed59e70d701c23ec5ab3dbdd456c251db87c053cdb19a0b85f25865c8a521449`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7c4ac515d3c1caa54b3c5efff798405199528903b25da0683bc1ceafd804c`  
		Last Modified: Thu, 16 Mar 2023 02:43:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c43833f6ad6290de9bca7cdef2fd42e3fdc360425aee0cc0c5610f335873e`  
		Last Modified: Thu, 16 Mar 2023 02:43:18 GMT  
		Size: 258.5 KB (258471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338595f61a4f73430e7935e55fd6a4e9ed2ab7cab265310c9c90f41b00b94686`  
		Last Modified: Thu, 16 Mar 2023 02:43:26 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:be1492b0401753ac150dfa176689b9f9197e2555a1c0358626bde3c061ed4d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:397850dd721f2d70f2666b6034e38902616f1811810b36c57856e53a045e9260
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570f9463ec5d93718c4ef20e1a5a0bb21677e80bc18d56c0e717c38e26c8b4c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a90083e3034d3bc1b9cd93ac980645679a1506f873cd25e8759b770d6a61461`  
		Last Modified: Wed, 01 Mar 2023 16:46:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eeeb799d1653042b93fdcd8ddddf38f470636f27f9bfbd8ee44094494d5bd035
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea6141601a32ef3e9ddb787af10b16777d10e6f802f5ea43b2e1ad73737a2db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925b171a5b6905f2fc1f92e540bf573a7d1c4abc9b736557f021bfa3e6d337a`  
		Last Modified: Wed, 01 Mar 2023 05:02:21 GMT  
		Size: 11.3 MB (11313063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8074c66e9c1c6d7c8bc897638e24177c3359558c6def15f4b9d8b2137991e199`  
		Last Modified: Wed, 01 Mar 2023 05:02:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f84e6f64a3c5a3ef49889b62a805b3c3dedf301c1f9f42427ca1a0eadce9bd`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b890c89e5f8fe91006ffd4b6803b48d623054d8ed9388ac80d0e139ad4c7059`  
		Last Modified: Wed, 01 Mar 2023 05:02:20 GMT  
		Size: 311.8 KB (311811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759b54753a4731feb4431d567233efa66a2581b07b96efd4dda8f8525a0ee65`  
		Last Modified: Wed, 01 Mar 2023 05:02:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:c99a320f5b489b4b9fd685aa70c861a8e77a3129f3bb1c530d0922b327c88221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0ffafd9fe3daf7efd5f712fc3d053b225086b1827a78e47db5a7431e4be36f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdf78211984955858995b9d812f932ac9d4b78d162415e9b8f88e9d3cb9507`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b922cad3fe5d3b4160ae7b3a5e81a57639a85513db1e474d1ec0eef9c6590bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d236ae8b1b48090ac45a3c137236d2519bd66c888ac05b2259490ed82bab035a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:01:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c660fc12919553d4c7aa5bc89004fe56e8844231dce893e94984fe56dc23`  
		Last Modified: Wed, 01 Mar 2023 05:03:00 GMT  
		Size: 11.7 MB (11661138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19c97c2997b743d321faeb9616b3a6e870b9fce608c572197aeab2f394c594`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9217cf8b3cf849d5480f0b028fe5a6a95663fa518c91e44ada3d8c7e086baf`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a238e1cc1f54ddef9247ec8bf508b59a49995e1564a673f8947751096ea9f5`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 282.2 KB (282223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:f528b19cc612f1d1444e5a4e3a3acf883bfca110b57d86b7f6f1e244c844f371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62722827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5387b36ce2af622c1e0eba8fe0b4347ccf401180723bdcb1bd9eee565933a3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:b2d0ed22177b3c3c8cb5d6d6a25905af2773c600258c137a9793979a87c1ae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:afa4b10de84e23db29f6f1b7d6ef28195645f359c8bd6a4e0262ddb6fcc5a597
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f356db77ba481cb1de7195e9ed0a895d3b289dde5a5d61a99dcba2b2c8b33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06941c2c76256cec7bbde5b3f998444239e34aa3cfd46afe763196c5dcba4b36`  
		Last Modified: Wed, 01 Mar 2023 16:47:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9fc9ba0c241d8f9728643ff32c6917a453ccbc5c41dabcd51275bf322a03d2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476fcee5f96b3a7ad70dee55321deb7000b054866b61a10148784d9f7d2f4d52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:01:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c660fc12919553d4c7aa5bc89004fe56e8844231dce893e94984fe56dc23`  
		Last Modified: Wed, 01 Mar 2023 05:03:00 GMT  
		Size: 11.7 MB (11661138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19c97c2997b743d321faeb9616b3a6e870b9fce608c572197aeab2f394c594`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9217cf8b3cf849d5480f0b028fe5a6a95663fa518c91e44ada3d8c7e086baf`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a238e1cc1f54ddef9247ec8bf508b59a49995e1564a673f8947751096ea9f5`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 282.2 KB (282223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9240d83d2e30f2e3699c4bc43a52d90ccd538a47c8632e6b90692688dfff0af4`  
		Last Modified: Wed, 01 Mar 2023 05:03:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf1388217fc75201eec1764ecf9ccc9d84becbc1a5c2fff97de123176d113bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5280e2b5efae98def7467cf9eecfc70f505f631e134aee484003dfdb9202f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61643c2ab05c90ffcc0f8e261d002b4cd8d654267ceadef7f14d5b5f46a05348`  
		Last Modified: Wed, 01 Mar 2023 14:25:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
