## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:9e60a3007bfabe50e8f2e366cef0d0297b34904e7b4880f39a16fd24529eea29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:917c5ae7b60b328a63cecd4eb385e1f713f23098c90670f2293a967b9633093c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86426210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5269e6bd4eb9dae1d4063ff31665600eef31956a07caf3e1813f1d2c08a755`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:47 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:49 GMT
ADD file:7d5373d4ccc5f70f68afa885a495329e33f2bf9f97a437251cfc79e7b85a1a88 in / 
# Tue, 01 Aug 2023 05:32:49 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:34:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:316675922a661ce4c35389bdeea6e9ec8d4708e41f08671b586c7aaea469b2c1`  
		Last Modified: Thu, 03 Aug 2023 03:40:24 GMT  
		Size: 27.9 MB (27857084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7def12313ae9d69537ed1d4ea003f137f16c5789329735bfd447f8c86cfca`  
		Last Modified: Thu, 03 Aug 2023 03:40:22 GMT  
		Size: 13.8 MB (13783649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476103e20eaed817175054747eac1aeb5b843e57c0d9a11994cdf770c7fba77d`  
		Last Modified: Thu, 03 Aug 2023 03:40:39 GMT  
		Size: 44.8 MB (44785477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b12d55cb3ad2cc317f455358e1e9f2347408daec65d87c5d708010884bdfd34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87019854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc3d99f07701bb3b5e6320d0bf9f458a22c0de934d0a362f8b698562be52083`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:25:35 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:25:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:25:40 GMT
ADD file:87326fc74610678eef05e8f4de7077af56538e06f1edcd35cdc95393dbe4a1fb in / 
# Tue, 01 Aug 2023 05:25:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:19:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:50dee684667fc0747a5dc7177b696c42d34b3d08a440f3413a53280696d07c9b`  
		Last Modified: Thu, 03 Aug 2023 01:26:11 GMT  
		Size: 25.4 MB (25380789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4208e441245229820b0d3ba5fd394d70ba11ed5aca02778ed20f1b5de6af6`  
		Last Modified: Thu, 03 Aug 2023 01:26:09 GMT  
		Size: 12.7 MB (12700472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b461fd4f3360e0033899510d338d7e5ed255815bd3715558c3a68d2a433c6c0`  
		Last Modified: Thu, 03 Aug 2023 01:26:28 GMT  
		Size: 48.9 MB (48938593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c41c51b6ab982df780eae8161be6d38a64dcfa31eb5e1da76d36ac1df2f6bb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85267114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5e0c1c9ff336e4af720d7c08a9d1426f9825eb87fe1790baa88644d9a773da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:59:38 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:59:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:59:47 GMT
ADD file:a621d5a90b1c5e05eb41dfa44616425f9e9c474acc76e148c36a525e99ff2bac in / 
# Mon, 07 Aug 2023 16:59:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b4647be7125cb643de6d0a75158905d697da4afc1e9edcd35dbb27a43edf604`  
		Last Modified: Wed, 16 Aug 2023 01:42:51 GMT  
		Size: 27.3 MB (27266349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f74bc0fb029a079dcd558844cc26c5973e7ec9efc2db4555c60ab536a1a11f`  
		Last Modified: Wed, 16 Aug 2023 01:42:49 GMT  
		Size: 13.4 MB (13369802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7156641b60d58d063ba957dec8ada8f9f2a4052eae760ec0c791b84480868de1`  
		Last Modified: Wed, 16 Aug 2023 01:43:05 GMT  
		Size: 44.6 MB (44630963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4136e3817a6ca408b13fac1da01a8d002ecb99ee64c880a0fa0227775e2af2ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97562897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee4aaf792deb5f130bf51d9a628aa47b399dc8231f64e8d739b6e55cea0efac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:10 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:13 GMT
ADD file:10d789d1b719d7a401c55c5b0aa22be71267e703ab44185d257d5615fb643c6f in / 
# Tue, 01 Aug 2023 05:33:13 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:40:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8970c2c49565e20d33a2f8309ce6ae16b1060876e805ac82902576e8850baff`  
		Last Modified: Thu, 03 Aug 2023 03:53:30 GMT  
		Size: 32.1 MB (32129425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67beaefc29343717c657c826614bdf12b09a224d01dd9917fba89b8d0beedb5`  
		Last Modified: Thu, 03 Aug 2023 03:53:26 GMT  
		Size: 15.9 MB (15880605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1f9973ab1d8bb4a0527af2ef0c6efea1bfd7c6e8e5ef18787d18c18f7db91`  
		Last Modified: Thu, 03 Aug 2023 03:53:55 GMT  
		Size: 49.6 MB (49552867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e2be1e684ed36c83a4386aed999d61829b37672df08deb3e2c9c27db3efef6da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85405385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b3dac9f5150bdd8c702d3cad0ab14d4105892e87f5443890e8b335b1b11217`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:48 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:48 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:50 GMT
ADD file:dd263eea5d15c08fe1aa830f7313ad188951ffe22caabbf664edfa2459c63b99 in / 
# Tue, 01 Aug 2023 05:32:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 00:17:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da7f02973684568dd47cf916af8e79783f8ec0ce768358ad7dd50a79e2090c53`  
		Last Modified: Thu, 03 Aug 2023 00:22:47 GMT  
		Size: 26.5 MB (26537706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ca0e17cab3bf50e237aea2fbaac414404d2f0cef2fc329f9eaa94169a777cd`  
		Last Modified: Thu, 03 Aug 2023 00:22:45 GMT  
		Size: 14.1 MB (14052687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6814bfc1e50d3e20bf4c3b19a6345b45a53e9774fd7596694ae808bbf81bb66`  
		Last Modified: Thu, 03 Aug 2023 00:23:01 GMT  
		Size: 44.8 MB (44814992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
