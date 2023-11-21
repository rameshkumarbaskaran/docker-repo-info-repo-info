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
$ docker pull neurodebian@sha256:0dc0c6379aa9de4c7beb314a77836296ed1b9ecec52b6e370d7d1d8fb37e8c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:436d0f91b2596d1a67587f416d172e20ea63d2ba9fab4064134e658283be40b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54202678ffa323cabbfa7d9142d688755ff6767f3a44607c1eb821edd05ac91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be402681584b912cb441771e9a7e1b039e2da347fe7ebf2d1cd9f3736c2e5b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364f14a0ddb6cdd1d2222f8d8d1cd397a7334c3eb47c91b89028ee7a7e491380`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:c6e4772e5c601ede7ccf289927f339f34eab81e04942d3e803f285f931926a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:137b909d0e4c4e1c4300fa4479a22b15c053df24cbbef0f13fce395100eafa77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226a853426c1d4b6bd2f86d099a28d4c4db35b9d83d9a7021c549f5386248a11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e158a3949abb4a78460b0321777ca278a50c79ac290966e5d6a7f027b04e3dd`  
		Last Modified: Fri, 02 Jun 2023 01:35:57 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edc6bddeb118195088c3f1948fdc52cc913d453e5f543927c7c89c015fe7bd6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d966d5bec6e766760870e6f4674ca17b3fe69617f78ade07c2a7b6b3154ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:46:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350adb1f8b3dcaa1835899b2dc84ec2f5a997c31b87aa8e76470a92bc742bc7f`  
		Last Modified: Thu, 01 Jun 2023 23:46:55 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:e35e1ebda0157d635121200ce782aef2aaf789aa070c229ddba2a563e1188f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:0acf4ccd7979f181031416378268c9d195dcd26fcac771e9c385e8ba18b2e905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc12c40eeddd04e825a714126de916daac07b5608eb8c1efd509e1381a6d923d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd67eface08324388119bee4f10bb75e9a6619d8217046470a8846f7b65fd55b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc21bc3b5d17a6427aa32b7aa7c2b96fa6a07d76bea9ccf7c7b09a8b7743de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a05b8e97c67453a0a55a42f69b0e567db2d0752c265c7a5c5f219e1855cd0`  
		Last Modified: Wed, 01 Nov 2023 11:30:19 GMT  
		Size: 11.4 MB (11429427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed9bd84f33819020b7286ee3228a6129c3742dfaaa3bc6fefc6f18622bb024`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9780640c8ae3cecbbd1a655dd9311877765283fbb03b209664e4dbf8117b6e83`  
		Last Modified: Wed, 01 Nov 2023 11:30:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec84b69a62a84a36c9bdb39cb2b2d7586f0912ec40efe2801100ab801f5896f`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 289.9 KB (289948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:369e44778bbd257e64b5d2bb9debe0e889697c1e5bab81215b1feba527c8487c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eebfddc39f59d3ea468a60b211da66a5c1ea8522beeffbc621dcb832e1dae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54672849c6fbb653b54ed8563dd39c70f075d13deabdd15a3c0d8b34cf1c5d0f`  
		Last Modified: Wed, 01 Nov 2023 14:13:04 GMT  
		Size: 11.9 MB (11885540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be2903537d6c97210103968fcff93892f8f70224543c01714513f7262ab60`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e905684323f5f1d0f41fb0502c3f005ba7f99f845da0326c6478eee4b1ef1f`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d83607efb9119cc84d9c28730d2c4c2028e131ec0a40f7721f13f89351a0a`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 289.7 KB (289720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:a3cbd769414f19c1e06c3d80309270c82065f28f78ea776ecca3e7a6caccf41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:daca28e2bfbee68d3ed03e1149fed58854a35c8e017aa7c3830cc98a5692e04a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d21c45fc808ee273991a96c58abfc74db29136c49f8831fc527b3e81e968f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe21bee7eb327ee7ef767c20d799f1b61cc7084dceb58906b8a1c4b2b6ff5379`  
		Last Modified: Tue, 21 Nov 2023 09:04:30 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765d8be459dfe7b2785af5336f4b8765be8752a47758ae534bfedd885f70ecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b499da7e192bcb5144c2560ce4ef14a88e6efeb77ab7852a736e26e02aaa0892`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a05b8e97c67453a0a55a42f69b0e567db2d0752c265c7a5c5f219e1855cd0`  
		Last Modified: Wed, 01 Nov 2023 11:30:19 GMT  
		Size: 11.4 MB (11429427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed9bd84f33819020b7286ee3228a6129c3742dfaaa3bc6fefc6f18622bb024`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9780640c8ae3cecbbd1a655dd9311877765283fbb03b209664e4dbf8117b6e83`  
		Last Modified: Wed, 01 Nov 2023 11:30:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec84b69a62a84a36c9bdb39cb2b2d7586f0912ec40efe2801100ab801f5896f`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 289.9 KB (289948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6aa21dba7165099dd051c8932d2845680b607124940a916cb35e77582c57d1`  
		Last Modified: Wed, 01 Nov 2023 11:30:27 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f8f74ee1d14cb47fffe6bb3dcd7ab472dcff9f03407e0be1a27ee48ce721ce63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faca678135925cc1ffd112cd88f40e43a92863ba55c6bc6b4b941b6d1ee78b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54672849c6fbb653b54ed8563dd39c70f075d13deabdd15a3c0d8b34cf1c5d0f`  
		Last Modified: Wed, 01 Nov 2023 14:13:04 GMT  
		Size: 11.9 MB (11885540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be2903537d6c97210103968fcff93892f8f70224543c01714513f7262ab60`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e905684323f5f1d0f41fb0502c3f005ba7f99f845da0326c6478eee4b1ef1f`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d83607efb9119cc84d9c28730d2c4c2028e131ec0a40f7721f13f89351a0a`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 289.7 KB (289720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9827b3c0bcb7754bd753b835acc6e59ea615605bd4e2d4873ee9cde2cceb3`  
		Last Modified: Wed, 01 Nov 2023 14:13:13 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:c1df6719c854f2e082442a7ad0ff793ccbfd003e6174789dc0f99bf9a996f817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff78b09dee0b90b68a9263d13b8350bb4a753960b2775177ebdcc49c4a951a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66679765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd101dbad321af8efd6976b2e659f4c1be93cadc61522907f5f6d73dbc5f3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ca7f4728beeda83b04034bd987114ed1d734058018fd6262201029b5a852d515
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aebb2a8bba3b9fad89934bf5220c2241ffe9f7a1e3aa5adcb91fb1e19489a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:9a67b9eddbec6a7347a262ef43d5fe9eadb6d3b9465ab65ae7f7e4de61dabd95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac241a8df4b25e46eee15e020db434f386d431634cf9b5047b27097e69f4b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:b66774c0b2da2b629a3ea1f8526284f30a93d968c83be2da376c48eaa6dc5385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:efc5185ea1ea0315adfca08f92d57371878abcfca6c32ab5b4b51e2ed4fbf319
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9274fa4dd6ba4308dd1ddad6b420ce33c66cba0a81e60de0e9f49ec9338ae54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2e70bf7609d3493c50eba4ba8870a2d45f74b0a94ece0dda543b8c88132f84`  
		Last Modified: Tue, 21 Nov 2023 09:04:10 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9cb15b194da81e73a7bc555e1aba739ca44ab08e1460b99807bd7d79cbeae794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367b6dbb4a0d4cd561394fb567215803f00ab2024fad0d79be1d09cda37240a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f7fa6b57db4435901ab55ff8fb2650c2f7f8373b0b8b76aff97ad570f941ef`  
		Last Modified: Wed, 01 Nov 2023 11:30:07 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:15845407331c1eaa9b3dc02e76723532e7f0a22823cef2ccaa4eac625a76c8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68065188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ef6e22d51fc4e71082397c2738c26f122486edf587eb04cf49652f6b796332`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18994b809a7a0be623f8753068fb9b01e428604e33a1d38a604750ffacb957e`  
		Last Modified: Wed, 01 Nov 2023 14:12:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:622983e58061fda6c21605c533ae30c986658fbae02e229b4f0a345f9c232282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:da62d250fd4bdf2f3c34cecc214e8f50772f12149c9e64cc20a940062067f165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61305745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a80b9dbcdc7ea48e99524ee929708c0367b66db19f7f708bbc81c49d79300`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:01:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f451a3934dd4e405d1dde860ba51678368513b19573aff4a31e37ec0366b9d`  
		Last Modified: Tue, 21 Nov 2023 09:03:41 GMT  
		Size: 10.5 MB (10504804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4affb99dfb075e560f9c1cb0540086f42280fcb523cb1ad9b1e4dacdc7a6370a`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075cc32496ec9687c5bb5438c0ff3f5d35a14bae9d664a4632b8701809cb9c6e`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46c61d3ea200904ddfcadddf54a73182bcd89e26c3f9857dd1d7de8d66f8df`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 299.5 KB (299459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:65ff09ea62f27d174a9ab498b66f8e078c539e277d72dde120be1d784d0b33d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cdfc9c3f3e4a4074d910f9e1a11f5fb576f177779f1c74e9cef6d7b6e7fcd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929f0a42bee1218ebcc451261cd112239c22bce8e4e163dfacbc1c27fb0ff111`  
		Last Modified: Wed, 01 Nov 2023 11:29:36 GMT  
		Size: 10.5 MB (10510591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0a85c2b7105ae379c7ce849dff682eb5c233ad7046b7f6fd728edf5fab473`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47702ffaad8de982eefaca460984971aaac1b75d371e36a8d74b7ee70f74618`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64014833cfbdf221ad8a1aeaa21acf2dc6632670a2febd0ff9837ddb3c079b24`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 299.5 KB (299470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:91c07532cf1013b2a5d3e0affd7c4ee02b97d9dbf44c1788b926e9934b3a2a37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab632dcec2afd39112eba2164ad07a4e49ab1b2a10d40f881f3090b9b036e3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:28 GMT
ADD file:65beb9bd9a5ca258316260fb802c65d9c3cc4a9137e0a09a873d4404d5b24fcc in / 
# Wed, 01 Nov 2023 00:39:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:10:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:10:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:10:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e1a1831feefb5bd8f0a9fbc43f06ac287e16d9dd672e28d11eb17f3df2c71cd`  
		Last Modified: Wed, 01 Nov 2023 00:44:36 GMT  
		Size: 51.3 MB (51255735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ef6d732ba4bbf5156b8005a11f6de7e2477e577eb2e81fac37427f0476f2b`  
		Last Modified: Wed, 01 Nov 2023 14:12:20 GMT  
		Size: 10.9 MB (10868533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157768b74ec360d0169d4615617bfd749cd0a00bf099fc8cd4765c0136f61c10`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ef45fc10c3c16a2412eb5bebc83c8ba1d047722ffb129d20497e2d2f72c7b`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861269c00680ca59edd0e5436a3da0eda7172e8aa4c5005d527c661e08bb55`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 299.4 KB (299420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:4ea6e91f12ee7b6a1673a0ef0f0d06a41f4c650b56058cf397ab82547169b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:015c6c1cc85fe77c9bf7cfac3a71d81441d6011b48fd8af491d5efebe58df567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc6cf45b421d833f34f46e9776df6ffa3e4839d11708fcdb858b9f2e5e5c94c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:01:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f451a3934dd4e405d1dde860ba51678368513b19573aff4a31e37ec0366b9d`  
		Last Modified: Tue, 21 Nov 2023 09:03:41 GMT  
		Size: 10.5 MB (10504804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4affb99dfb075e560f9c1cb0540086f42280fcb523cb1ad9b1e4dacdc7a6370a`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075cc32496ec9687c5bb5438c0ff3f5d35a14bae9d664a4632b8701809cb9c6e`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46c61d3ea200904ddfcadddf54a73182bcd89e26c3f9857dd1d7de8d66f8df`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 299.5 KB (299459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250d20ae10895f11051d1c47eeba40930a3e4ca156e7609546071bdb9ac65f3`  
		Last Modified: Tue, 21 Nov 2023 09:03:50 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a555dc09947275c11494d2bb70ed9532a7de199e588b60b172e788cf68940893
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b06e9f434fbf483d930e71ecef0c745a559fc518d6d1cc68849a1e302afe27a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929f0a42bee1218ebcc451261cd112239c22bce8e4e163dfacbc1c27fb0ff111`  
		Last Modified: Wed, 01 Nov 2023 11:29:36 GMT  
		Size: 10.5 MB (10510591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0a85c2b7105ae379c7ce849dff682eb5c233ad7046b7f6fd728edf5fab473`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47702ffaad8de982eefaca460984971aaac1b75d371e36a8d74b7ee70f74618`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64014833cfbdf221ad8a1aeaa21acf2dc6632670a2febd0ff9837ddb3c079b24`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 299.5 KB (299470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d883c980f09c5f8536563a950d31207595ca88fbc8fe6bebfc3420c96ec7c2`  
		Last Modified: Wed, 01 Nov 2023 11:29:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f826c6ff907a386eb33425bd363662209c40516c78eec07885bb65f549750d9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e232f9f7c0e240703b957ebeb7e90b87178f032631ae7a3a001f1802dd33acb7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:28 GMT
ADD file:65beb9bd9a5ca258316260fb802c65d9c3cc4a9137e0a09a873d4404d5b24fcc in / 
# Wed, 01 Nov 2023 00:39:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:10:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:10:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:10:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2e1a1831feefb5bd8f0a9fbc43f06ac287e16d9dd672e28d11eb17f3df2c71cd`  
		Last Modified: Wed, 01 Nov 2023 00:44:36 GMT  
		Size: 51.3 MB (51255735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ef6d732ba4bbf5156b8005a11f6de7e2477e577eb2e81fac37427f0476f2b`  
		Last Modified: Wed, 01 Nov 2023 14:12:20 GMT  
		Size: 10.9 MB (10868533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157768b74ec360d0169d4615617bfd749cd0a00bf099fc8cd4765c0136f61c10`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ef45fc10c3c16a2412eb5bebc83c8ba1d047722ffb129d20497e2d2f72c7b`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861269c00680ca59edd0e5436a3da0eda7172e8aa4c5005d527c661e08bb55`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 299.4 KB (299420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d1c81b8ccfc7670bc3e1e96a65ffb89a83e4ae674abad99cfe34577127ed21`  
		Last Modified: Wed, 01 Nov 2023 14:12:28 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:ed83527c5b9c4b8395127c1633336bb594a64120f02d68b3e57414c0619e7e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d8a9a2bcb9bfb6bd074eecfcdd1ca62d718e7a66b8161b9f0cee1bb5ee566a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0446001e7b7eef2aadec7e87784e91f57bc35eb51fd9f001a0d23237f3c83822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:29:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:29:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd85b9bbb4f6a9a09f01ff35c38ff6c009e4ed47c1e1adb561e5e1881ef6329`  
		Last Modified: Fri, 13 Oct 2023 08:31:16 GMT  
		Size: 5.5 MB (5494637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82d4dfa24a3aa971caf981cc84ea5292b7c56b4335194a635a745d12cf335e`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e62499f00f9e5e824ea39061aa4a173eb1dea821e53978d30d32377cfdb483`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecfaed538c1437570df4d09b720ce5fc7a1516d14bf689952efdb1882979b2`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 239.4 KB (239434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a9f7cb59ff4b081a48587e48b6210b3d4af02f876cea8fa47623c31506f852b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32916777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea9511dcba80f806f6a8c5cf40a1cf3a089faf1c5c6b65423b1d5dea211c0f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:55:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735b752a5a5ddf2e2a73ae4efa42262f0bc4d0c1d75658b76770451fc0458f6a`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 5.5 MB (5475192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3041aaece1d5937a215d07e3f1fc08de72687caf87826635325e5c8f7f45418c`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da06e0720e864bbf2fbae18550b7e7877c71a63f413c7ee1d76240441c64895`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43168bfd26889b61874a4ae799abf4489eb95c11265e131ec5b50d6971d9a819`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 240.1 KB (240069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:7d92c9ebe90a7c6f708b792ea78fadf4a1ee38d449b8ff9d6a5bc703f4f94b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e073e031a4a6d9a0ba2e8698883a93d78f7f02605dce5429e06938d0c3a696f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34317018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3615da31fcee40f87efbe02509455a6357ffbe41d7f9ea2805858013d9bd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:29:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:29:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd85b9bbb4f6a9a09f01ff35c38ff6c009e4ed47c1e1adb561e5e1881ef6329`  
		Last Modified: Fri, 13 Oct 2023 08:31:16 GMT  
		Size: 5.5 MB (5494637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82d4dfa24a3aa971caf981cc84ea5292b7c56b4335194a635a745d12cf335e`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e62499f00f9e5e824ea39061aa4a173eb1dea821e53978d30d32377cfdb483`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecfaed538c1437570df4d09b720ce5fc7a1516d14bf689952efdb1882979b2`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 239.4 KB (239434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be323d4e6d5888beb53bc54cb02411f80710e117bd8b93dd3fbd147bde90cb`  
		Last Modified: Fri, 13 Oct 2023 08:31:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07d82819b71e813a5458133a08ac64541f6f6e9a15fd4b3820a02e8fb49f945d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32917032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0af1ce5b729930583866de774b375ed677e0ccee5d9799aa876e8bf8877c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:55:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735b752a5a5ddf2e2a73ae4efa42262f0bc4d0c1d75658b76770451fc0458f6a`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 5.5 MB (5475192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3041aaece1d5937a215d07e3f1fc08de72687caf87826635325e5c8f7f45418c`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da06e0720e864bbf2fbae18550b7e7877c71a63f413c7ee1d76240441c64895`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43168bfd26889b61874a4ae799abf4489eb95c11265e131ec5b50d6971d9a819`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 240.1 KB (240069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4f4e3657a300eddb3d58745b4ef645b6bdf391f63bb940bf63fe58cff0b930`  
		Last Modified: Fri, 13 Oct 2023 02:56:56 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:b4d49e7360eb0c2b42ffa98f7d39d5a10678aa8150eda796a5a7f1ab4dd39307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e2aa73f9f09af2566980b8e495f0b8b62a814d92a8f8ca16eb0aaf20d9067c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0452d17a83582c40d2cafd271986a859967fed1c986a0c26f566ea5e2767fb51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:30:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:30:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:30:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e0384b0751c689672d93e3a583d0f82f563ac76ed169e1b8c3698e7c1b9ae`  
		Last Modified: Fri, 13 Oct 2023 08:31:33 GMT  
		Size: 3.8 MB (3766206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1965fb1bd982ac95de3cd97df09921e2b37180acca64f9c5e1caeda6fd12d5`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950979dba938d002077c91ca72ca18a4664cfd04d00f60b1eab5492177c7292`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbe240e1948f0756efdec7579645345b9d490ccec6616989ab5b75cc57f237`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 252.7 KB (252718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a79d1953fe207f196ad06744c4c494d2f1626e2ec4433fc5dc3731c13596955d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32387822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13669db7a906a6d32ec74e7122de0dd2db8ba365dcc760349c70dd67919c2955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:56:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c9d9fd32f7ed46ec165bfc72630fe971f719e63fdf4324845082dbd1caa79`  
		Last Modified: Fri, 13 Oct 2023 02:57:07 GMT  
		Size: 3.7 MB (3739822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c61a34bfc1eb01fd98e89934398ac55d28f86554556cef06331a761cc6d70e`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d61c0ded99806942b23025d926d8999759a391a63a30c5222665142865bc9b`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17795fbc1348d7ec52019935cb1ffef48e3a4bfb7de209dcba5705b765e8d374`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 254.0 KB (254049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:d90a567d896ae8458af57b4eaa7348c24f28729eef29d2c796ec8b8559ace49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d19e02ca380df295118a29cf49008e7182baef13299515df4343f8c333facf42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0dc2fdcfad3f544074530b54c34e17c233cb103abb3161a74770af036a03b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:30:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:30:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:30:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e0384b0751c689672d93e3a583d0f82f563ac76ed169e1b8c3698e7c1b9ae`  
		Last Modified: Fri, 13 Oct 2023 08:31:33 GMT  
		Size: 3.8 MB (3766206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1965fb1bd982ac95de3cd97df09921e2b37180acca64f9c5e1caeda6fd12d5`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950979dba938d002077c91ca72ca18a4664cfd04d00f60b1eab5492177c7292`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbe240e1948f0756efdec7579645345b9d490ccec6616989ab5b75cc57f237`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 252.7 KB (252718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822627743fb03ddc3332e67ae9f02bacc3e10492b6bf42de83ca0ff2a5ac727c`  
		Last Modified: Fri, 13 Oct 2023 08:31:41 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9e80ac0e889f0b22dc738027acb83a7597ae5df857a894d9435c6d241804b6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32388082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54645d0e87bfb204cb9fa74f02b97ac04ebd11821f26ffede361201d69aa5ded`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:56:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:56:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c9d9fd32f7ed46ec165bfc72630fe971f719e63fdf4324845082dbd1caa79`  
		Last Modified: Fri, 13 Oct 2023 02:57:07 GMT  
		Size: 3.7 MB (3739822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c61a34bfc1eb01fd98e89934398ac55d28f86554556cef06331a761cc6d70e`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d61c0ded99806942b23025d926d8999759a391a63a30c5222665142865bc9b`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17795fbc1348d7ec52019935cb1ffef48e3a4bfb7de209dcba5705b765e8d374`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 254.0 KB (254049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5165f39871dd6953ccde2fcaae90a14aaf51cd4204eac033b3c6c135e56b670`  
		Last Modified: Fri, 13 Oct 2023 02:57:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:c1df6719c854f2e082442a7ad0ff793ccbfd003e6174789dc0f99bf9a996f817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff78b09dee0b90b68a9263d13b8350bb4a753960b2775177ebdcc49c4a951a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66679765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd101dbad321af8efd6976b2e659f4c1be93cadc61522907f5f6d73dbc5f3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ca7f4728beeda83b04034bd987114ed1d734058018fd6262201029b5a852d515
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aebb2a8bba3b9fad89934bf5220c2241ffe9f7a1e3aa5adcb91fb1e19489a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:9a67b9eddbec6a7347a262ef43d5fe9eadb6d3b9465ab65ae7f7e4de61dabd95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac241a8df4b25e46eee15e020db434f386d431634cf9b5047b27097e69f4b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:2211f7b0a4c6172a0ddd9554b7f15f4bf21f3bd7034bb0f3e8453688e09bf04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:1ecd936078dd03fdfa2fd6c8064cf1a36fd1eef4d36f2c933e001d0ea055e8e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca526f0ef2949aaa012342d3d6e431c73334d7b42c0d4279ffe7a6d9d02580bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:006d33d4cab788adeee6911fcb02d8563ab6e0fe507da912966d5d461e99d9a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c69d5a54cf71cbae75f0afc2782c2e2c33de8ede1b251fed10ce3f865db07c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:45 GMT
ADD file:1a4ef85bba464538c4f87a65a055d954fc8edc51f26efd06b43d8ae9f7e54f7a in / 
# Wed, 01 Nov 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba6956ade110f0fe56bbad19a8d10b1eb0ae1b1006ccba5fadff0026a00dbc20`  
		Last Modified: Wed, 01 Nov 2023 00:45:46 GMT  
		Size: 49.6 MB (49552835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fbbac0d173796cda178a2a5a16ef5653fd220176a8c1565a0e86578dfd5b43`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 14.1 MB (14110787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ad058d489d17b39a4da4559d4d1da74e03361e46fa5e3670d997ec2851b10d`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f70086a1d7c6eaf83af96a052b81bf45319b8dc5ed934fe6f18df5d0b9ee2cb`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72569af24d4890ff6a8af7435d326bafb016e91e61cceff66cadaa06b017c6b3`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 286.4 KB (286401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:0f215c08c074257983247d45ae7fd57d3d7bee8210b48cc3c616924f18470b6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4759a872b53a56d1c0765b65a6a61bc25f988f2685ef37416bfdfc5e179103`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877103b070021622926ceb6f8c3c90cb54008a01d4f93ad524a0c443ba8d9e1`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 14.7 MB (14693007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aead82d4a1d86b5570bfe854c2cdc25ad8587bd580270277f34845096dcaa3`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a94cb01393d4cb28efba9612f6b12752b3fb9734cdd6ea4e7f36a05579a1b`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e63f83cc7265a6e3ab79ca141dcc92d5ec8517daf06c55bc4d9e8997d349a52`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 285.8 KB (285785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:6436e2cd38ae48b8160c187fc3ff8c95c309f2a27a52e8058c269c96db1bc714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8bf257824aefa8385ad61f019be968c3ad774b46de888ffc6a0289f589144be0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b299f8fa9025b01fda6c1a485c3d1d8ae5587c500753eb30e0d3fb7912b860e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2248e03a81aac3ef875d327ae662c63d1e610cff26c081cb48860b88ee6b82`  
		Last Modified: Tue, 21 Nov 2023 09:04:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b60b35b544c37e3992af9ba8f34583a596793ff6f3baa73fd2f496fabe4100b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534c5c4f00ea7262fb367c1afe91f242add4bbbcce3c0903e2e3f56012396f70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:45 GMT
ADD file:1a4ef85bba464538c4f87a65a055d954fc8edc51f26efd06b43d8ae9f7e54f7a in / 
# Wed, 01 Nov 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:29:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ba6956ade110f0fe56bbad19a8d10b1eb0ae1b1006ccba5fadff0026a00dbc20`  
		Last Modified: Wed, 01 Nov 2023 00:45:46 GMT  
		Size: 49.6 MB (49552835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fbbac0d173796cda178a2a5a16ef5653fd220176a8c1565a0e86578dfd5b43`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 14.1 MB (14110787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ad058d489d17b39a4da4559d4d1da74e03361e46fa5e3670d997ec2851b10d`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f70086a1d7c6eaf83af96a052b81bf45319b8dc5ed934fe6f18df5d0b9ee2cb`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72569af24d4890ff6a8af7435d326bafb016e91e61cceff66cadaa06b017c6b3`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 286.4 KB (286401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c467fbd63429b91d1c94869d85f3dbc1a01abf80c565ed8574b528fa3e4e2bf`  
		Last Modified: Wed, 01 Nov 2023 11:30:47 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:765bedd8ad9fd50f88255f3e66a2f9cd314566d7416674410c7080ba696f0949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f32c55cc6e5c976db991420e7d86161e651507d7b223814a1194009768866f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877103b070021622926ceb6f8c3c90cb54008a01d4f93ad524a0c443ba8d9e1`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 14.7 MB (14693007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aead82d4a1d86b5570bfe854c2cdc25ad8587bd580270277f34845096dcaa3`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a94cb01393d4cb28efba9612f6b12752b3fb9734cdd6ea4e7f36a05579a1b`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e63f83cc7265a6e3ab79ca141dcc92d5ec8517daf06c55bc4d9e8997d349a52`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 285.8 KB (285785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb85209cdfc5de75c6ca3d659f345803ac19324b5c644a094ecdad5d271b4e94`  
		Last Modified: Wed, 01 Nov 2023 14:13:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:622983e58061fda6c21605c533ae30c986658fbae02e229b4f0a345f9c232282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:da62d250fd4bdf2f3c34cecc214e8f50772f12149c9e64cc20a940062067f165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61305745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a80b9dbcdc7ea48e99524ee929708c0367b66db19f7f708bbc81c49d79300`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:01:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f451a3934dd4e405d1dde860ba51678368513b19573aff4a31e37ec0366b9d`  
		Last Modified: Tue, 21 Nov 2023 09:03:41 GMT  
		Size: 10.5 MB (10504804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4affb99dfb075e560f9c1cb0540086f42280fcb523cb1ad9b1e4dacdc7a6370a`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075cc32496ec9687c5bb5438c0ff3f5d35a14bae9d664a4632b8701809cb9c6e`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46c61d3ea200904ddfcadddf54a73182bcd89e26c3f9857dd1d7de8d66f8df`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 299.5 KB (299459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:65ff09ea62f27d174a9ab498b66f8e078c539e277d72dde120be1d784d0b33d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cdfc9c3f3e4a4074d910f9e1a11f5fb576f177779f1c74e9cef6d7b6e7fcd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929f0a42bee1218ebcc451261cd112239c22bce8e4e163dfacbc1c27fb0ff111`  
		Last Modified: Wed, 01 Nov 2023 11:29:36 GMT  
		Size: 10.5 MB (10510591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0a85c2b7105ae379c7ce849dff682eb5c233ad7046b7f6fd728edf5fab473`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47702ffaad8de982eefaca460984971aaac1b75d371e36a8d74b7ee70f74618`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64014833cfbdf221ad8a1aeaa21acf2dc6632670a2febd0ff9837ddb3c079b24`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 299.5 KB (299470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:91c07532cf1013b2a5d3e0affd7c4ee02b97d9dbf44c1788b926e9934b3a2a37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab632dcec2afd39112eba2164ad07a4e49ab1b2a10d40f881f3090b9b036e3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:28 GMT
ADD file:65beb9bd9a5ca258316260fb802c65d9c3cc4a9137e0a09a873d4404d5b24fcc in / 
# Wed, 01 Nov 2023 00:39:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:10:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:10:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:10:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e1a1831feefb5bd8f0a9fbc43f06ac287e16d9dd672e28d11eb17f3df2c71cd`  
		Last Modified: Wed, 01 Nov 2023 00:44:36 GMT  
		Size: 51.3 MB (51255735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ef6d732ba4bbf5156b8005a11f6de7e2477e577eb2e81fac37427f0476f2b`  
		Last Modified: Wed, 01 Nov 2023 14:12:20 GMT  
		Size: 10.9 MB (10868533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157768b74ec360d0169d4615617bfd749cd0a00bf099fc8cd4765c0136f61c10`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ef45fc10c3c16a2412eb5bebc83c8ba1d047722ffb129d20497e2d2f72c7b`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861269c00680ca59edd0e5436a3da0eda7172e8aa4c5005d527c661e08bb55`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 299.4 KB (299420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:4ea6e91f12ee7b6a1673a0ef0f0d06a41f4c650b56058cf397ab82547169b0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:015c6c1cc85fe77c9bf7cfac3a71d81441d6011b48fd8af491d5efebe58df567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc6cf45b421d833f34f46e9776df6ffa3e4839d11708fcdb858b9f2e5e5c94c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:01:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f451a3934dd4e405d1dde860ba51678368513b19573aff4a31e37ec0366b9d`  
		Last Modified: Tue, 21 Nov 2023 09:03:41 GMT  
		Size: 10.5 MB (10504804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4affb99dfb075e560f9c1cb0540086f42280fcb523cb1ad9b1e4dacdc7a6370a`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075cc32496ec9687c5bb5438c0ff3f5d35a14bae9d664a4632b8701809cb9c6e`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46c61d3ea200904ddfcadddf54a73182bcd89e26c3f9857dd1d7de8d66f8df`  
		Last Modified: Tue, 21 Nov 2023 09:03:40 GMT  
		Size: 299.5 KB (299459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250d20ae10895f11051d1c47eeba40930a3e4ca156e7609546071bdb9ac65f3`  
		Last Modified: Tue, 21 Nov 2023 09:03:50 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a555dc09947275c11494d2bb70ed9532a7de199e588b60b172e788cf68940893
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b06e9f434fbf483d930e71ecef0c745a559fc518d6d1cc68849a1e302afe27a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929f0a42bee1218ebcc451261cd112239c22bce8e4e163dfacbc1c27fb0ff111`  
		Last Modified: Wed, 01 Nov 2023 11:29:36 GMT  
		Size: 10.5 MB (10510591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0a85c2b7105ae379c7ce849dff682eb5c233ad7046b7f6fd728edf5fab473`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47702ffaad8de982eefaca460984971aaac1b75d371e36a8d74b7ee70f74618`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64014833cfbdf221ad8a1aeaa21acf2dc6632670a2febd0ff9837ddb3c079b24`  
		Last Modified: Wed, 01 Nov 2023 11:29:35 GMT  
		Size: 299.5 KB (299470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d883c980f09c5f8536563a950d31207595ca88fbc8fe6bebfc3420c96ec7c2`  
		Last Modified: Wed, 01 Nov 2023 11:29:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f826c6ff907a386eb33425bd363662209c40516c78eec07885bb65f549750d9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62426054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e232f9f7c0e240703b957ebeb7e90b87178f032631ae7a3a001f1802dd33acb7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:28 GMT
ADD file:65beb9bd9a5ca258316260fb802c65d9c3cc4a9137e0a09a873d4404d5b24fcc in / 
# Wed, 01 Nov 2023 00:39:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:10:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:10:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:10:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:10:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2e1a1831feefb5bd8f0a9fbc43f06ac287e16d9dd672e28d11eb17f3df2c71cd`  
		Last Modified: Wed, 01 Nov 2023 00:44:36 GMT  
		Size: 51.3 MB (51255735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ef6d732ba4bbf5156b8005a11f6de7e2477e577eb2e81fac37427f0476f2b`  
		Last Modified: Wed, 01 Nov 2023 14:12:20 GMT  
		Size: 10.9 MB (10868533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157768b74ec360d0169d4615617bfd749cd0a00bf099fc8cd4765c0136f61c10`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ef45fc10c3c16a2412eb5bebc83c8ba1d047722ffb129d20497e2d2f72c7b`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861269c00680ca59edd0e5436a3da0eda7172e8aa4c5005d527c661e08bb55`  
		Last Modified: Wed, 01 Nov 2023 14:12:18 GMT  
		Size: 299.4 KB (299420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d1c81b8ccfc7670bc3e1e96a65ffb89a83e4ae674abad99cfe34577127ed21`  
		Last Modified: Wed, 01 Nov 2023 14:12:28 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:c1df6719c854f2e082442a7ad0ff793ccbfd003e6174789dc0f99bf9a996f817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff78b09dee0b90b68a9263d13b8350bb4a753960b2775177ebdcc49c4a951a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66679765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd101dbad321af8efd6976b2e659f4c1be93cadc61522907f5f6d73dbc5f3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ca7f4728beeda83b04034bd987114ed1d734058018fd6262201029b5a852d515
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aebb2a8bba3b9fad89934bf5220c2241ffe9f7a1e3aa5adcb91fb1e19489a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:9a67b9eddbec6a7347a262ef43d5fe9eadb6d3b9465ab65ae7f7e4de61dabd95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac241a8df4b25e46eee15e020db434f386d431634cf9b5047b27097e69f4b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:b66774c0b2da2b629a3ea1f8526284f30a93d968c83be2da376c48eaa6dc5385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:efc5185ea1ea0315adfca08f92d57371878abcfca6c32ab5b4b51e2ed4fbf319
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9274fa4dd6ba4308dd1ddad6b420ce33c66cba0a81e60de0e9f49ec9338ae54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2e70bf7609d3493c50eba4ba8870a2d45f74b0a94ece0dda543b8c88132f84`  
		Last Modified: Tue, 21 Nov 2023 09:04:10 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9cb15b194da81e73a7bc555e1aba739ca44ab08e1460b99807bd7d79cbeae794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367b6dbb4a0d4cd561394fb567215803f00ab2024fad0d79be1d09cda37240a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f7fa6b57db4435901ab55ff8fb2650c2f7f8373b0b8b76aff97ad570f941ef`  
		Last Modified: Wed, 01 Nov 2023 11:30:07 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:15845407331c1eaa9b3dc02e76723532e7f0a22823cef2ccaa4eac625a76c8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68065188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ef6e22d51fc4e71082397c2738c26f122486edf587eb04cf49652f6b796332`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18994b809a7a0be623f8753068fb9b01e428604e33a1d38a604750ffacb957e`  
		Last Modified: Wed, 01 Nov 2023 14:12:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:e35e1ebda0157d635121200ce782aef2aaf789aa070c229ddba2a563e1188f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:0acf4ccd7979f181031416378268c9d195dcd26fcac771e9c385e8ba18b2e905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc12c40eeddd04e825a714126de916daac07b5608eb8c1efd509e1381a6d923d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd67eface08324388119bee4f10bb75e9a6619d8217046470a8846f7b65fd55b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc21bc3b5d17a6427aa32b7aa7c2b96fa6a07d76bea9ccf7c7b09a8b7743de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a05b8e97c67453a0a55a42f69b0e567db2d0752c265c7a5c5f219e1855cd0`  
		Last Modified: Wed, 01 Nov 2023 11:30:19 GMT  
		Size: 11.4 MB (11429427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed9bd84f33819020b7286ee3228a6129c3742dfaaa3bc6fefc6f18622bb024`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9780640c8ae3cecbbd1a655dd9311877765283fbb03b209664e4dbf8117b6e83`  
		Last Modified: Wed, 01 Nov 2023 11:30:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec84b69a62a84a36c9bdb39cb2b2d7586f0912ec40efe2801100ab801f5896f`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 289.9 KB (289948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:369e44778bbd257e64b5d2bb9debe0e889697c1e5bab81215b1feba527c8487c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eebfddc39f59d3ea468a60b211da66a5c1ea8522beeffbc621dcb832e1dae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54672849c6fbb653b54ed8563dd39c70f075d13deabdd15a3c0d8b34cf1c5d0f`  
		Last Modified: Wed, 01 Nov 2023 14:13:04 GMT  
		Size: 11.9 MB (11885540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be2903537d6c97210103968fcff93892f8f70224543c01714513f7262ab60`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e905684323f5f1d0f41fb0502c3f005ba7f99f845da0326c6478eee4b1ef1f`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d83607efb9119cc84d9c28730d2c4c2028e131ec0a40f7721f13f89351a0a`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 289.7 KB (289720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:a3cbd769414f19c1e06c3d80309270c82065f28f78ea776ecca3e7a6caccf41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:daca28e2bfbee68d3ed03e1149fed58854a35c8e017aa7c3830cc98a5692e04a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d21c45fc808ee273991a96c58abfc74db29136c49f8831fc527b3e81e968f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe21bee7eb327ee7ef767c20d799f1b61cc7084dceb58906b8a1c4b2b6ff5379`  
		Last Modified: Tue, 21 Nov 2023 09:04:30 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765d8be459dfe7b2785af5336f4b8765be8752a47758ae534bfedd885f70ecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b499da7e192bcb5144c2560ce4ef14a88e6efeb77ab7852a736e26e02aaa0892`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a05b8e97c67453a0a55a42f69b0e567db2d0752c265c7a5c5f219e1855cd0`  
		Last Modified: Wed, 01 Nov 2023 11:30:19 GMT  
		Size: 11.4 MB (11429427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed9bd84f33819020b7286ee3228a6129c3742dfaaa3bc6fefc6f18622bb024`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9780640c8ae3cecbbd1a655dd9311877765283fbb03b209664e4dbf8117b6e83`  
		Last Modified: Wed, 01 Nov 2023 11:30:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec84b69a62a84a36c9bdb39cb2b2d7586f0912ec40efe2801100ab801f5896f`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 289.9 KB (289948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6aa21dba7165099dd051c8932d2845680b607124940a916cb35e77582c57d1`  
		Last Modified: Wed, 01 Nov 2023 11:30:27 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f8f74ee1d14cb47fffe6bb3dcd7ab472dcff9f03407e0be1a27ee48ce721ce63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faca678135925cc1ffd112cd88f40e43a92863ba55c6bc6b4b941b6d1ee78b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54672849c6fbb653b54ed8563dd39c70f075d13deabdd15a3c0d8b34cf1c5d0f`  
		Last Modified: Wed, 01 Nov 2023 14:13:04 GMT  
		Size: 11.9 MB (11885540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be2903537d6c97210103968fcff93892f8f70224543c01714513f7262ab60`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e905684323f5f1d0f41fb0502c3f005ba7f99f845da0326c6478eee4b1ef1f`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d83607efb9119cc84d9c28730d2c4c2028e131ec0a40f7721f13f89351a0a`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 289.7 KB (289720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9827b3c0bcb7754bd753b835acc6e59ea615605bd4e2d4873ee9cde2cceb3`  
		Last Modified: Wed, 01 Nov 2023 14:13:13 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:0dc0c6379aa9de4c7beb314a77836296ed1b9ecec52b6e370d7d1d8fb37e8c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:436d0f91b2596d1a67587f416d172e20ea63d2ba9fab4064134e658283be40b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54202678ffa323cabbfa7d9142d688755ff6767f3a44607c1eb821edd05ac91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:be402681584b912cb441771e9a7e1b039e2da347fe7ebf2d1cd9f3736c2e5b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364f14a0ddb6cdd1d2222f8d8d1cd397a7334c3eb47c91b89028ee7a7e491380`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:c6e4772e5c601ede7ccf289927f339f34eab81e04942d3e803f285f931926a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:137b909d0e4c4e1c4300fa4479a22b15c053df24cbbef0f13fce395100eafa77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31780770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226a853426c1d4b6bd2f86d099a28d4c4db35b9d83d9a7021c549f5386248a11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:34:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Jun 2023 01:34:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Jun 2023 01:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:34:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fd3f50024409b1b68a3a6f4702400bd9a64d841513f895cc7d024105b78cc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 4.8 MB (4821090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc489477c8d20c6f0b75906068dc8bd8fe67e1f59f73730d062182879ae588fc`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e27f6db7ca8cf1f438fd944f25c4f24e021afb589cc28a0069a6dff45807a5`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b84f628a2b60e2cd65ca99d9064b0cf13b65787e82747dad9fa68a2e0f016`  
		Last Modified: Fri, 02 Jun 2023 01:35:49 GMT  
		Size: 240.2 KB (240158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e158a3949abb4a78460b0321777ca278a50c79ac290966e5d6a7f027b04e3dd`  
		Last Modified: Fri, 02 Jun 2023 01:35:57 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edc6bddeb118195088c3f1948fdc52cc913d453e5f543927c7c89c015fe7bd6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28385761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d966d5bec6e766760870e6f4674ca17b3fe69617f78ade07c2a7b6b3154ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Jun 2023 23:45:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Jun 2023 23:45:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:46:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca58392fb171b1b6480d0e939cedf1babf2bd1d61cbc5fd8667f30d13cf1e73`  
		Last Modified: Thu, 01 Jun 2023 23:46:48 GMT  
		Size: 4.4 MB (4402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833dbaa1fde66205ef9230adea619512493c576ac6baf435bdb3dc21e1072e1d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a674c5e1cc8e1b1dcc8a4daacac73e2c8748f8babf74d3cfff92c15ba68e4d`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce993d3dfac320106ebff10dddff6363ba6d572101bb95c51d321564439c7b`  
		Last Modified: Thu, 01 Jun 2023 23:46:47 GMT  
		Size: 240.0 KB (240022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350adb1f8b3dcaa1835899b2dc84ec2f5a997c31b87aa8e76470a92bc742bc7f`  
		Last Modified: Thu, 01 Jun 2023 23:46:55 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:ed83527c5b9c4b8395127c1633336bb594a64120f02d68b3e57414c0619e7e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d8a9a2bcb9bfb6bd074eecfcdd1ca62d718e7a66b8161b9f0cee1bb5ee566a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34316763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0446001e7b7eef2aadec7e87784e91f57bc35eb51fd9f001a0d23237f3c83822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:29:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:29:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd85b9bbb4f6a9a09f01ff35c38ff6c009e4ed47c1e1adb561e5e1881ef6329`  
		Last Modified: Fri, 13 Oct 2023 08:31:16 GMT  
		Size: 5.5 MB (5494637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82d4dfa24a3aa971caf981cc84ea5292b7c56b4335194a635a745d12cf335e`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e62499f00f9e5e824ea39061aa4a173eb1dea821e53978d30d32377cfdb483`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecfaed538c1437570df4d09b720ce5fc7a1516d14bf689952efdb1882979b2`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 239.4 KB (239434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2a9f7cb59ff4b081a48587e48b6210b3d4af02f876cea8fa47623c31506f852b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32916777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea9511dcba80f806f6a8c5cf40a1cf3a089faf1c5c6b65423b1d5dea211c0f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:55:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735b752a5a5ddf2e2a73ae4efa42262f0bc4d0c1d75658b76770451fc0458f6a`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 5.5 MB (5475192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3041aaece1d5937a215d07e3f1fc08de72687caf87826635325e5c8f7f45418c`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da06e0720e864bbf2fbae18550b7e7877c71a63f413c7ee1d76240441c64895`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43168bfd26889b61874a4ae799abf4489eb95c11265e131ec5b50d6971d9a819`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 240.1 KB (240069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:7d92c9ebe90a7c6f708b792ea78fadf4a1ee38d449b8ff9d6a5bc703f4f94b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e073e031a4a6d9a0ba2e8698883a93d78f7f02605dce5429e06938d0c3a696f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34317018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3615da31fcee40f87efbe02509455a6357ffbe41d7f9ea2805858013d9bd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:29:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:29:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd85b9bbb4f6a9a09f01ff35c38ff6c009e4ed47c1e1adb561e5e1881ef6329`  
		Last Modified: Fri, 13 Oct 2023 08:31:16 GMT  
		Size: 5.5 MB (5494637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82d4dfa24a3aa971caf981cc84ea5292b7c56b4335194a635a745d12cf335e`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e62499f00f9e5e824ea39061aa4a173eb1dea821e53978d30d32377cfdb483`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecfaed538c1437570df4d09b720ce5fc7a1516d14bf689952efdb1882979b2`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 239.4 KB (239434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be323d4e6d5888beb53bc54cb02411f80710e117bd8b93dd3fbd147bde90cb`  
		Last Modified: Fri, 13 Oct 2023 08:31:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07d82819b71e813a5458133a08ac64541f6f6e9a15fd4b3820a02e8fb49f945d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32917032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0af1ce5b729930583866de774b375ed677e0ccee5d9799aa876e8bf8877c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:55:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735b752a5a5ddf2e2a73ae4efa42262f0bc4d0c1d75658b76770451fc0458f6a`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 5.5 MB (5475192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3041aaece1d5937a215d07e3f1fc08de72687caf87826635325e5c8f7f45418c`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da06e0720e864bbf2fbae18550b7e7877c71a63f413c7ee1d76240441c64895`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43168bfd26889b61874a4ae799abf4489eb95c11265e131ec5b50d6971d9a819`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 240.1 KB (240069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4f4e3657a300eddb3d58745b4ef645b6bdf391f63bb940bf63fe58cff0b930`  
		Last Modified: Fri, 13 Oct 2023 02:56:56 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:b4d49e7360eb0c2b42ffa98f7d39d5a10678aa8150eda796a5a7f1ab4dd39307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e2aa73f9f09af2566980b8e495f0b8b62a814d92a8f8ca16eb0aaf20d9067c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0452d17a83582c40d2cafd271986a859967fed1c986a0c26f566ea5e2767fb51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:30:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:30:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:30:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e0384b0751c689672d93e3a583d0f82f563ac76ed169e1b8c3698e7c1b9ae`  
		Last Modified: Fri, 13 Oct 2023 08:31:33 GMT  
		Size: 3.8 MB (3766206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1965fb1bd982ac95de3cd97df09921e2b37180acca64f9c5e1caeda6fd12d5`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950979dba938d002077c91ca72ca18a4664cfd04d00f60b1eab5492177c7292`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbe240e1948f0756efdec7579645345b9d490ccec6616989ab5b75cc57f237`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 252.7 KB (252718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a79d1953fe207f196ad06744c4c494d2f1626e2ec4433fc5dc3731c13596955d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32387822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13669db7a906a6d32ec74e7122de0dd2db8ba365dcc760349c70dd67919c2955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:56:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c9d9fd32f7ed46ec165bfc72630fe971f719e63fdf4324845082dbd1caa79`  
		Last Modified: Fri, 13 Oct 2023 02:57:07 GMT  
		Size: 3.7 MB (3739822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c61a34bfc1eb01fd98e89934398ac55d28f86554556cef06331a761cc6d70e`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d61c0ded99806942b23025d926d8999759a391a63a30c5222665142865bc9b`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17795fbc1348d7ec52019935cb1ffef48e3a4bfb7de209dcba5705b765e8d374`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 254.0 KB (254049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:d90a567d896ae8458af57b4eaa7348c24f28729eef29d2c796ec8b8559ace49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d19e02ca380df295118a29cf49008e7182baef13299515df4343f8c333facf42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0dc2fdcfad3f544074530b54c34e17c233cb103abb3161a74770af036a03b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:30:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:30:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:30:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e0384b0751c689672d93e3a583d0f82f563ac76ed169e1b8c3698e7c1b9ae`  
		Last Modified: Fri, 13 Oct 2023 08:31:33 GMT  
		Size: 3.8 MB (3766206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1965fb1bd982ac95de3cd97df09921e2b37180acca64f9c5e1caeda6fd12d5`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950979dba938d002077c91ca72ca18a4664cfd04d00f60b1eab5492177c7292`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbe240e1948f0756efdec7579645345b9d490ccec6616989ab5b75cc57f237`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 252.7 KB (252718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822627743fb03ddc3332e67ae9f02bacc3e10492b6bf42de83ca0ff2a5ac727c`  
		Last Modified: Fri, 13 Oct 2023 08:31:41 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9e80ac0e889f0b22dc738027acb83a7597ae5df857a894d9435c6d241804b6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32388082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54645d0e87bfb204cb9fa74f02b97ac04ebd11821f26ffede361201d69aa5ded`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:56:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:56:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c9d9fd32f7ed46ec165bfc72630fe971f719e63fdf4324845082dbd1caa79`  
		Last Modified: Fri, 13 Oct 2023 02:57:07 GMT  
		Size: 3.7 MB (3739822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c61a34bfc1eb01fd98e89934398ac55d28f86554556cef06331a761cc6d70e`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d61c0ded99806942b23025d926d8999759a391a63a30c5222665142865bc9b`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17795fbc1348d7ec52019935cb1ffef48e3a4bfb7de209dcba5705b765e8d374`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 254.0 KB (254049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5165f39871dd6953ccde2fcaae90a14aaf51cd4204eac033b3c6c135e56b670`  
		Last Modified: Fri, 13 Oct 2023 02:57:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b66774c0b2da2b629a3ea1f8526284f30a93d968c83be2da376c48eaa6dc5385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:efc5185ea1ea0315adfca08f92d57371878abcfca6c32ab5b4b51e2ed4fbf319
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9274fa4dd6ba4308dd1ddad6b420ce33c66cba0a81e60de0e9f49ec9338ae54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2e70bf7609d3493c50eba4ba8870a2d45f74b0a94ece0dda543b8c88132f84`  
		Last Modified: Tue, 21 Nov 2023 09:04:10 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9cb15b194da81e73a7bc555e1aba739ca44ab08e1460b99807bd7d79cbeae794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367b6dbb4a0d4cd561394fb567215803f00ab2024fad0d79be1d09cda37240a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a7a3efaa0b614824a277c87b0b0645ce498231b25d127472f8cf1b21374e7`  
		Last Modified: Wed, 01 Nov 2023 11:29:55 GMT  
		Size: 11.3 MB (11313485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8928ed4b25edde54e1a30259c987b3907a9401f34f2de6997924fa54aa4`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8480b77e6f1e64715dbf9ebca0833cf162349bac0acbe1012e7ef0b6e7f8`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88e1c6d85ec9d08368ac3c6cd436ec0aef8357548e6aec6c58b2bc942b11dd`  
		Last Modified: Wed, 01 Nov 2023 11:29:54 GMT  
		Size: 307.9 KB (307873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f7fa6b57db4435901ab55ff8fb2650c2f7f8373b0b8b76aff97ad570f941ef`  
		Last Modified: Wed, 01 Nov 2023 11:30:07 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:15845407331c1eaa9b3dc02e76723532e7f0a22823cef2ccaa4eac625a76c8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68065188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ef6e22d51fc4e71082397c2738c26f122486edf587eb04cf49652f6b796332`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1bade1ceaf1308d48cac6e1db51a90d6c9586e404a0c5deff39516b9c2839`  
		Last Modified: Wed, 01 Nov 2023 14:12:39 GMT  
		Size: 11.7 MB (11708782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517537fc7369742d54ac6e7721db2ac5b7d421b05b88117d68e7eb6908aec0a2`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c5930ebf3cf79db0817b91e206b68c0a5a796e05096b9a63d70d5e2d39b36`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82c65cfa29da10be5abf1fb2893b920d4f0ec1648df5770465fc47406f8515d`  
		Last Modified: Wed, 01 Nov 2023 14:12:37 GMT  
		Size: 307.8 KB (307768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18994b809a7a0be623f8753068fb9b01e428604e33a1d38a604750ffacb957e`  
		Last Modified: Wed, 01 Nov 2023 14:12:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:2211f7b0a4c6172a0ddd9554b7f15f4bf21f3bd7034bb0f3e8453688e09bf04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:1ecd936078dd03fdfa2fd6c8064cf1a36fd1eef4d36f2c933e001d0ea055e8e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca526f0ef2949aaa012342d3d6e431c73334d7b42c0d4279ffe7a6d9d02580bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:006d33d4cab788adeee6911fcb02d8563ab6e0fe507da912966d5d461e99d9a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c69d5a54cf71cbae75f0afc2782c2e2c33de8ede1b251fed10ce3f865db07c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:45 GMT
ADD file:1a4ef85bba464538c4f87a65a055d954fc8edc51f26efd06b43d8ae9f7e54f7a in / 
# Wed, 01 Nov 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba6956ade110f0fe56bbad19a8d10b1eb0ae1b1006ccba5fadff0026a00dbc20`  
		Last Modified: Wed, 01 Nov 2023 00:45:46 GMT  
		Size: 49.6 MB (49552835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fbbac0d173796cda178a2a5a16ef5653fd220176a8c1565a0e86578dfd5b43`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 14.1 MB (14110787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ad058d489d17b39a4da4559d4d1da74e03361e46fa5e3670d997ec2851b10d`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f70086a1d7c6eaf83af96a052b81bf45319b8dc5ed934fe6f18df5d0b9ee2cb`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72569af24d4890ff6a8af7435d326bafb016e91e61cceff66cadaa06b017c6b3`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 286.4 KB (286401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:0f215c08c074257983247d45ae7fd57d3d7bee8210b48cc3c616924f18470b6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4759a872b53a56d1c0765b65a6a61bc25f988f2685ef37416bfdfc5e179103`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877103b070021622926ceb6f8c3c90cb54008a01d4f93ad524a0c443ba8d9e1`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 14.7 MB (14693007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aead82d4a1d86b5570bfe854c2cdc25ad8587bd580270277f34845096dcaa3`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a94cb01393d4cb28efba9612f6b12752b3fb9734cdd6ea4e7f36a05579a1b`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e63f83cc7265a6e3ab79ca141dcc92d5ec8517daf06c55bc4d9e8997d349a52`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 285.8 KB (285785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:6436e2cd38ae48b8160c187fc3ff8c95c309f2a27a52e8058c269c96db1bc714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8bf257824aefa8385ad61f019be968c3ad774b46de888ffc6a0289f589144be0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b299f8fa9025b01fda6c1a485c3d1d8ae5587c500753eb30e0d3fb7912b860e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2248e03a81aac3ef875d327ae662c63d1e610cff26c081cb48860b88ee6b82`  
		Last Modified: Tue, 21 Nov 2023 09:04:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b60b35b544c37e3992af9ba8f34583a596793ff6f3baa73fd2f496fabe4100b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534c5c4f00ea7262fb367c1afe91f242add4bbbcce3c0903e2e3f56012396f70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:45 GMT
ADD file:1a4ef85bba464538c4f87a65a055d954fc8edc51f26efd06b43d8ae9f7e54f7a in / 
# Wed, 01 Nov 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:29:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ba6956ade110f0fe56bbad19a8d10b1eb0ae1b1006ccba5fadff0026a00dbc20`  
		Last Modified: Wed, 01 Nov 2023 00:45:46 GMT  
		Size: 49.6 MB (49552835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fbbac0d173796cda178a2a5a16ef5653fd220176a8c1565a0e86578dfd5b43`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 14.1 MB (14110787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ad058d489d17b39a4da4559d4d1da74e03361e46fa5e3670d997ec2851b10d`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f70086a1d7c6eaf83af96a052b81bf45319b8dc5ed934fe6f18df5d0b9ee2cb`  
		Last Modified: Wed, 01 Nov 2023 11:30:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72569af24d4890ff6a8af7435d326bafb016e91e61cceff66cadaa06b017c6b3`  
		Last Modified: Wed, 01 Nov 2023 11:30:36 GMT  
		Size: 286.4 KB (286401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c467fbd63429b91d1c94869d85f3dbc1a01abf80c565ed8574b528fa3e4e2bf`  
		Last Modified: Wed, 01 Nov 2023 11:30:47 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:765bedd8ad9fd50f88255f3e66a2f9cd314566d7416674410c7080ba696f0949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f32c55cc6e5c976db991420e7d86161e651507d7b223814a1194009768866f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877103b070021622926ceb6f8c3c90cb54008a01d4f93ad524a0c443ba8d9e1`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 14.7 MB (14693007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aead82d4a1d86b5570bfe854c2cdc25ad8587bd580270277f34845096dcaa3`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a94cb01393d4cb28efba9612f6b12752b3fb9734cdd6ea4e7f36a05579a1b`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e63f83cc7265a6e3ab79ca141dcc92d5ec8517daf06c55bc4d9e8997d349a52`  
		Last Modified: Wed, 01 Nov 2023 14:13:22 GMT  
		Size: 285.8 KB (285785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb85209cdfc5de75c6ca3d659f345803ac19324b5c644a094ecdad5d271b4e94`  
		Last Modified: Wed, 01 Nov 2023 14:13:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
