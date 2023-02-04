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
$ docker pull neurodebian@sha256:e513ac1e11156aecac472db495f4a8a9289c483b45d0dc1b4a246b58da08ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:9eaae57e6a418b8c573fc5418ad64fe129309c35c2fd161bbdbf61a529730d9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31775229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873262071297edd49a7d33afe192f7dd416fbcb8f8329bfc9d17b220889f04e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:58:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:58:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:58:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c561dd565402593670454bc67f0d32877f005872b8d25d4a588ff0bd84d74582`  
		Last Modified: Tue, 31 Jan 2023 19:00:39 GMT  
		Size: 4.8 MB (4821347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199a21fc88a38a5953a4eda7d548104c2153dbacdbeac0c1f97636aa990429d`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4dc3134d8a8ba0f045aa233e851c13346eb4ea771d8394c56cf2863567c2a8`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c014dbfdfc0e1f416ac41d8cf451e1463598f92d704b7440a38610c18f4ebe26`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 240.4 KB (240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5683ede91c2464e5b6ae9098e6c50ff505d17f1fa2f3e71b42ead7b3feccd26f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490edb93bb34812d94fffb01906d7d28c3e9fc0bb12c7cd49c911c949fa7ad3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:08:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:08:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:08:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbc19e87e6da7df7a26b73c38813e606d157ff82cead74668aa9fb1dde50fe`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 4.4 MB (4403764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13f880e3b2e22e0f79bd577aae93628955db5dfb54dc16b5ee01d78e283612`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1536cf9d0676d119194aaac6a84cfd3883f661525fc07c8c16507232e4b0820`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d9d3933a870d2b232e0931a36cc44e9dc946dd9f6dcdb07cc55b77f21a170`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 241.1 KB (241081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:691ca2cf102d15603a0c797e930a351ed9c873489a8ee27f1e76b43eadc33e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7c10782a79f7c72117a5374ce52548ca719f89305356417c7957eef4ce83a492
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31775483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6c7baace0050bff9e555573db23e79cca0226c59505907eb177d7fd551e1e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:58:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:58:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:58:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c561dd565402593670454bc67f0d32877f005872b8d25d4a588ff0bd84d74582`  
		Last Modified: Tue, 31 Jan 2023 19:00:39 GMT  
		Size: 4.8 MB (4821347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199a21fc88a38a5953a4eda7d548104c2153dbacdbeac0c1f97636aa990429d`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4dc3134d8a8ba0f045aa233e851c13346eb4ea771d8394c56cf2863567c2a8`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c014dbfdfc0e1f416ac41d8cf451e1463598f92d704b7440a38610c18f4ebe26`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 240.4 KB (240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb917c28cea7ae4fa4a9d361cbbd4494ecd182af107d7ee5936bcb018641040`  
		Last Modified: Tue, 31 Jan 2023 19:00:46 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0106f5e71d6be760cf4fa278aa89bf7ab086e4711f5751e8c9e46031e939ba69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15489cd4bee72086827d309d7fa524ab5f75084ac3a273f752ba9de140d3d70f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:08:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:08:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:08:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbc19e87e6da7df7a26b73c38813e606d157ff82cead74668aa9fb1dde50fe`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 4.4 MB (4403764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13f880e3b2e22e0f79bd577aae93628955db5dfb54dc16b5ee01d78e283612`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1536cf9d0676d119194aaac6a84cfd3883f661525fc07c8c16507232e4b0820`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d9d3933a870d2b232e0931a36cc44e9dc946dd9f6dcdb07cc55b77f21a170`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 241.1 KB (241081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3633341f6970cb9798062d7a3e8b9c338cf172ef3b05cdc69e65ba08a562aee`  
		Last Modified: Tue, 31 Jan 2023 18:10:39 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:d8d24c7d181ae38e6555701a6b2fe2e267ca8aba201e3dc252bc95aeadbe68fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:cd16c6aef63a3db7fcb7cfbab5887e0f81e4803627f8f549d8e038cb3086180b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132d235ab4814815386bbcab148ddd5655f36d30392713c800468fedd7472205`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:50:57 GMT
ADD file:59c477049f0246331c6723687b7f8995e7a8946172b967d10fb8b67146220c33 in / 
# Sat, 04 Feb 2023 06:50:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20aeb9ca89f41415a92cd1a5e9ff6c0280e09a250e0f950c9df57d97b0d3efb5`  
		Last Modified: Sat, 04 Feb 2023 06:55:19 GMT  
		Size: 49.0 MB (49043016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b130d3ba13f067628bc387a54a1da8af7b4a096ce82ec156552956e406d7b`  
		Last Modified: Sat, 04 Feb 2023 09:51:06 GMT  
		Size: 11.6 MB (11649256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b839812e578b5131df5e1fedba0bac2db5b86c439d3b9d5f60c8acc2138048`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301743227e61250a633af79548b62dd2e3731aeff84a7ab7b0731685356d6b7`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348a923b18932afef779b25fb09416eeba581400fa1b039bbbfd9f718d400590`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 280.8 KB (280824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47d7a6535244ad6e95e521fd44c18618793ed1aa080c1eead00b9dcd26032188
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0990886517f471603003c7bff9a8442a9624b45903ac2c0307fba5b87c4eaf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:08 GMT
ADD file:b40ad920bd7dd081e20adf36435db50381b9998a1de3d2eac6b2c45734ce60b3 in / 
# Sat, 04 Feb 2023 06:17:09 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a43b5d5927a7651097e784be4430a6ade09951f5b6879cd06b0f51fc7c4812af`  
		Last Modified: Sat, 04 Feb 2023 06:20:30 GMT  
		Size: 49.1 MB (49081538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178538c5bc5dcf98be54976e26e3643caa3a37f742386a75aeeda9818488236`  
		Last Modified: Sat, 04 Feb 2023 08:50:55 GMT  
		Size: 11.6 MB (11613318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946ba90fc15d686558f937d9db8c112910bfcc60659eae41906cab00536fbd1`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d06715673a85e222fe91b40adfd40e6cf12abad4d8fc6b94aa1a329f289b576`  
		Last Modified: Sat, 04 Feb 2023 08:50:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b2fd07b19b38ae39db22c7c35d3f8f01c22b33486483bc0f26dd2f8d1e600`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 281.2 KB (281229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:af1f08b15a4552a4640cc28b82c5191420f39a7e659135c335e428b94832823d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62069539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb9530c0e32632a30dbc1f4c5c64f3550af137d440eb9d9dc1049930dbbae9d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:48:40 GMT
ADD file:71f93fd08314b2207fb2e5840185c4db4279fa8f008742cf35eaf4daf925d475 in / 
# Sat, 04 Feb 2023 07:48:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b6e1871a6864b2026696c7ffe48da3030a97146a6a0f3ca18f87c19b1ed6e05`  
		Last Modified: Sat, 04 Feb 2023 07:53:55 GMT  
		Size: 50.1 MB (50093420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e4ba6446be2b949171fc2868a8c59235d2af1758d013151fcd57d081401b6`  
		Last Modified: Sat, 04 Feb 2023 10:20:10 GMT  
		Size: 11.9 MB (11882451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70715b74ec52eab8e28b9acfabf935edf643321adb523d3d69a98e9486900a52`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdff03b60b1edaee34f47a2f80a061b637fca4ae130e5261d8d7f7ced5c14b10`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24bbda6354a4d781c58506977ac567ec1b139d570de8854e2130234b8d3a3c1`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 91.7 KB (91680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:ec2e654afac39e54093ddc4ddacd1cafc57d08a81e85cbe42849140f172c5010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:038d27cd30b1fbc077e69ef71a2d03e5754e5d92cc86b17c271c0912c0952c1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9217cccc9e4b0cb5b096d954ca7a60e94975fa1f08693781a8f53d48e5fd908b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:50:57 GMT
ADD file:59c477049f0246331c6723687b7f8995e7a8946172b967d10fb8b67146220c33 in / 
# Sat, 04 Feb 2023 06:50:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:20aeb9ca89f41415a92cd1a5e9ff6c0280e09a250e0f950c9df57d97b0d3efb5`  
		Last Modified: Sat, 04 Feb 2023 06:55:19 GMT  
		Size: 49.0 MB (49043016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b130d3ba13f067628bc387a54a1da8af7b4a096ce82ec156552956e406d7b`  
		Last Modified: Sat, 04 Feb 2023 09:51:06 GMT  
		Size: 11.6 MB (11649256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b839812e578b5131df5e1fedba0bac2db5b86c439d3b9d5f60c8acc2138048`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301743227e61250a633af79548b62dd2e3731aeff84a7ab7b0731685356d6b7`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348a923b18932afef779b25fb09416eeba581400fa1b039bbbfd9f718d400590`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 280.8 KB (280824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd55eff8502d8c054050f00e802fa327dccdd4b4c08c28c44be57867702d11`  
		Last Modified: Sat, 04 Feb 2023 09:51:15 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d38cc525233e026ed1dc6ab33d626e38579465070da1b007a4377ad7e892c38
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f457705f06d5d27f6710a5d2077f18bec766f68fff56c944f7ad6428fca9b65`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:08 GMT
ADD file:b40ad920bd7dd081e20adf36435db50381b9998a1de3d2eac6b2c45734ce60b3 in / 
# Sat, 04 Feb 2023 06:17:09 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a43b5d5927a7651097e784be4430a6ade09951f5b6879cd06b0f51fc7c4812af`  
		Last Modified: Sat, 04 Feb 2023 06:20:30 GMT  
		Size: 49.1 MB (49081538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178538c5bc5dcf98be54976e26e3643caa3a37f742386a75aeeda9818488236`  
		Last Modified: Sat, 04 Feb 2023 08:50:55 GMT  
		Size: 11.6 MB (11613318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946ba90fc15d686558f937d9db8c112910bfcc60659eae41906cab00536fbd1`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d06715673a85e222fe91b40adfd40e6cf12abad4d8fc6b94aa1a329f289b576`  
		Last Modified: Sat, 04 Feb 2023 08:50:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b2fd07b19b38ae39db22c7c35d3f8f01c22b33486483bc0f26dd2f8d1e600`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 281.2 KB (281229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596e70a3c681969a418f4e81170b181a23350b8e71edecd45c416d7c429c37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:02 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f17948d0f4324a8463f4b46218f398ed9999a1286d1cd6a22634242bf24b268a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62069966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc12f02cb74b2e26e73e18689145b654a7cf1dc1e565925d1a7ff9962936f8f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:48:40 GMT
ADD file:71f93fd08314b2207fb2e5840185c4db4279fa8f008742cf35eaf4daf925d475 in / 
# Sat, 04 Feb 2023 07:48:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0b6e1871a6864b2026696c7ffe48da3030a97146a6a0f3ca18f87c19b1ed6e05`  
		Last Modified: Sat, 04 Feb 2023 07:53:55 GMT  
		Size: 50.1 MB (50093420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e4ba6446be2b949171fc2868a8c59235d2af1758d013151fcd57d081401b6`  
		Last Modified: Sat, 04 Feb 2023 10:20:10 GMT  
		Size: 11.9 MB (11882451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70715b74ec52eab8e28b9acfabf935edf643321adb523d3d69a98e9486900a52`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdff03b60b1edaee34f47a2f80a061b637fca4ae130e5261d8d7f7ced5c14b10`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24bbda6354a4d781c58506977ac567ec1b139d570de8854e2130234b8d3a3c1`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 91.7 KB (91680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18447a03ec0fb4ac174af8327d90f68ad4c4aeca490e18fc4e4aa1d779098d8d`  
		Last Modified: Sat, 04 Feb 2023 10:20:20 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:9dc880c2ce22a2f4c430a893feafb23b00c13c743504b131c579fbe93c96be05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:f136bdf78d08ec8cf0feb11966e5587135c56e56e6f3905d0e5e674d5dffb6a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f359014092dda5786bb73d03ef8cad9f9d4ff58ea91dadffe2b00c30525e3606`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05cb95459d66a096424e07c1ed40a5be080386293e1f332d98587b154f495795
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65308759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1dfad29a96eb0452204b34a699e432f876d5238fc40e3091e78c5e88867c1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:051d60da7defa64efef48b78723ea65f7b1d4702e7a4ccd4e77ab5960eb3fe7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67612855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d387f73e7e78a2311817f3bb4aefe8ee66e61ed3db81bd4b1215fb7225919`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:08fcd85f86870ee5e676210963d6d22e463e4a7db52d874e14cfd62bda8d5f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c993c02f8bc36311ce8c06e0498a78563fd21b0d9363cdbaec2663151ded439d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4276a71ae9be81384cbfd82a8237629fc4ab2189d7a976fb15ea1650dcce2c6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3516a1ee8523855e4dad47eb62eb2523c08e5866d617bbfedb1b1189f1a8d5`  
		Last Modified: Sat, 04 Feb 2023 09:50:55 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30cf133c2939a3e22c8c9c47f8a7e66b7e2ff19edf863a0431e3912e80c6d7d0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65309119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a13b8f85eea85993fd122f87cf1d2e938e7897346d1e1ad5a275adf7ef906d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f08233a2e298109671c3c73b17ab2cadfcf1339e4cdf03e2f98d3c5f0bb5c7`  
		Last Modified: Sat, 04 Feb 2023 08:50:44 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:20e38f1a665337e410e5460f17d7289aa230f54fadb417fa78ce750a4d14ac08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67613214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c34efe9a2aa1e621ff74f9ebf3f4767bba6652c4007239b6aa8e8d3cea1ab7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7507e9bb7871aaa80f25eeb282f3810619c9d58c28a042a6045d823903047`  
		Last Modified: Sat, 04 Feb 2023 10:19:56 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:20b1e4b385c295908c70bbc044e5efe1e77b360ba4955716cada49d307f79677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:b8cec976c7ae22d7eb1de919a8d17dda0ebb47bfb23ddf37e495bea5f5cf5413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8664646e57311fbef0fcca2b8a240ef4551469837bab7b884ac53b773f6cce29`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:48:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2c6114af2471df54db6a6f68996f51e5c6725dc13cd50218152e6b734fc9d`  
		Last Modified: Sat, 04 Feb 2023 09:50:29 GMT  
		Size: 10.5 MB (10504469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad61b917527e7bc9d3081b7d815d4312d7cd7b898cbb8a8a454c994afa032c`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894fb81d9c36b05fd865441fb72d450686bcabdd720cb053a0e26bfc4d172e9b`  
		Last Modified: Sat, 04 Feb 2023 09:50:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c75efa50c7d459603199041a9d1229bda46816a8c61d7e37754c14bf032d41`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 304.4 KB (304369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dc36f118472fb5e0b20c26b75d1bfbcf49480dfc7776c2e37ace4b31486be06d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f705abad5e5e4d726795ac15eae33baf5a4e1a515ff1054f4a3774e3fccc03fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda0b3f7673107c2204b83097e20a33728ef30d2e731e41727e0915eb8eb7c9`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 10.5 MB (10510366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e7e8e9562ff77a3d9a1bc9b20bcaaffb5ab25e375ce28460ba3a4018788fb`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c8ab4aac39ddf7a0f79a2cc135d4c299bb4a80b3282626e03ba7581e2ec733`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fc1d1a5e62555249343f0f0e4c5483c04f9b57bd28318895d6a9f14050a7e6`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 304.3 KB (304289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:e9ba4efba4fb4603470dfa4b361050c196a458e8db56b04b8482a6a5e3b49cba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61990982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef1323a087c0f2ec6cbfb43277e5eff5c495d0d796e6b0211e347ea7de54d8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b5157c7f1fe625aba139644ccc5d778bd2612aa09dbb07647cc8fb1645b7e2`  
		Last Modified: Sat, 04 Feb 2023 10:19:24 GMT  
		Size: 10.7 MB (10672599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c575c89dc25a96f058de33b540b31bcbcd0806e12baaa42524df5b83b25bb00`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549d3ced6edebcf3acdd958851b03298abe2d86782697f48fadf3ab90bd27f0`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4007a5e6d2ddd44a5c7d604ca425380f910138e3f9ccb53b3bb41818c2b57068`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 108.7 KB (108736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:5e21a5d696c2f24830b17ace2b22b92906df3aea7964965f403f18da363e180f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4eb056af4f99e5cf0e4bb36fb041598be17061b2f5badeb04de061d8a0d08e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65bb4c1dbc843123f57fbb6c227e448bf36bc91540efe30571d2e7373cd032`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:48:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2c6114af2471df54db6a6f68996f51e5c6725dc13cd50218152e6b734fc9d`  
		Last Modified: Sat, 04 Feb 2023 09:50:29 GMT  
		Size: 10.5 MB (10504469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad61b917527e7bc9d3081b7d815d4312d7cd7b898cbb8a8a454c994afa032c`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894fb81d9c36b05fd865441fb72d450686bcabdd720cb053a0e26bfc4d172e9b`  
		Last Modified: Sat, 04 Feb 2023 09:50:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c75efa50c7d459603199041a9d1229bda46816a8c61d7e37754c14bf032d41`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 304.4 KB (304369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d9bd0a1405d1b177e4fbba26da0f9cdde3947700b1810984c35e9b994dd984`  
		Last Modified: Sat, 04 Feb 2023 09:50:37 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9dbc4060d63354fc168ef4b4ce8d6572031d397dbd61b0240a71078697e7bc8d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e52ff1f01210e669f87eece484b274a1c9ed6dfe5aff7b6a0451113022b17b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda0b3f7673107c2204b83097e20a33728ef30d2e731e41727e0915eb8eb7c9`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 10.5 MB (10510366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e7e8e9562ff77a3d9a1bc9b20bcaaffb5ab25e375ce28460ba3a4018788fb`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c8ab4aac39ddf7a0f79a2cc135d4c299bb4a80b3282626e03ba7581e2ec733`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fc1d1a5e62555249343f0f0e4c5483c04f9b57bd28318895d6a9f14050a7e6`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 304.3 KB (304289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb106862c94d1d9cf42027a0b8de792e548f97d4bf206491e472fc6159c7e0e`  
		Last Modified: Sat, 04 Feb 2023 08:50:25 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6c16c1e38965d822f79bb63927ab57cf8eb2cbb537d907e84a89bbf24e1af8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2a0b1b021d82a33722be844bc6183dce33deab6f76ce2360e0f03a1e01fc2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b5157c7f1fe625aba139644ccc5d778bd2612aa09dbb07647cc8fb1645b7e2`  
		Last Modified: Sat, 04 Feb 2023 10:19:24 GMT  
		Size: 10.7 MB (10672599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c575c89dc25a96f058de33b540b31bcbcd0806e12baaa42524df5b83b25bb00`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549d3ced6edebcf3acdd958851b03298abe2d86782697f48fadf3ab90bd27f0`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4007a5e6d2ddd44a5c7d604ca425380f910138e3f9ccb53b3bb41818c2b57068`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 108.7 KB (108736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5f1cd364eb20620bd7ecfd8199b217eadb409140aa90a44a7e992a2c3e2c4`  
		Last Modified: Sat, 04 Feb 2023 10:19:33 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:fc0e3f6a31571b6faef75452e7b452d8bd6b64ec637462b7dc067544e4285a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:85b798bdb26eb6b1340fbc60fc0feec533e7dd20029f088b82cb4839a401cac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbceb465a22ad0be1c177c9fe16c5812526ba3dac6c3065f5eefbdd9efacfc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:32:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 19:32:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 19:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340633481010cfb4323a6980ddc3fbb99c2b231c2bae539ce3adbe4323848f34`  
		Last Modified: Wed, 01 Feb 2023 19:33:24 GMT  
		Size: 5.5 MB (5494456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a75d823acce0fa96f4fa88a59f0531577b8f2838bfe342fd493d768cbfcd`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1424e1c74c34cfbb9d0566bfa17947ded4bdff35d712e953ebe4b9a83f3483`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b985a598f6b1f9e18c76e8ff8ec2a3031cee1c84d02604bcde89fe5b75df28e4`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 238.9 KB (238907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f43cd8b79163c0d9d100aaf36b45be3a012257ff691d14de42300c681ff6862
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32909337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde545e728f21aeef32f65cf9201e112821ed623b0cd56fa89b9b5024752244`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:48:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 18:48:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 18:48:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5c02fa6b59ab2149fa6bd73b93cc90d70885b4c89395e276408e863c13469`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 5.5 MB (5474533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558f1a74caa43afa1ef7b67ba9f69563ea68ccc494931e60f17601e0d197766f`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc55772b4b9049168de57f770b06cdc6b133aad697a9d81fd887d0845d6b2e4`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64d2353b0251a8e328c31de617a38bc62b5f305270c4e614d42af92b1e1cc2b`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 239.1 KB (239055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:d60d4892922515af262d9b747b2b0c64622190e73ac678135285993f68ac0b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:168dd889aecd1f1d598a9b69160fa460d720c310f55b50eb7f132e76a28326b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7515b917b364356f96522dc926c5c828a4bf0df70fcf3945bd0f22f7fb7ba0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:32:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 19:32:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 19:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340633481010cfb4323a6980ddc3fbb99c2b231c2bae539ce3adbe4323848f34`  
		Last Modified: Wed, 01 Feb 2023 19:33:24 GMT  
		Size: 5.5 MB (5494456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a75d823acce0fa96f4fa88a59f0531577b8f2838bfe342fd493d768cbfcd`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1424e1c74c34cfbb9d0566bfa17947ded4bdff35d712e953ebe4b9a83f3483`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b985a598f6b1f9e18c76e8ff8ec2a3031cee1c84d02604bcde89fe5b75df28e4`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 238.9 KB (238907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dbb4dc6c7f0965eb4d15b6c9b5762a70d0caf0e9fca5b9eb8c5dbe3211b746`  
		Last Modified: Wed, 01 Feb 2023 19:33:31 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:757707483fe2ff4d1589194906a99b162fc40a8b19fe18f56b7e989510aae4c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32909592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e032ef358f0f25a08aba8f3214453113a399a57680920f1d06b130156139f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:48:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 18:48:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 18:48:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5c02fa6b59ab2149fa6bd73b93cc90d70885b4c89395e276408e863c13469`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 5.5 MB (5474533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558f1a74caa43afa1ef7b67ba9f69563ea68ccc494931e60f17601e0d197766f`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc55772b4b9049168de57f770b06cdc6b133aad697a9d81fd887d0845d6b2e4`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64d2353b0251a8e328c31de617a38bc62b5f305270c4e614d42af92b1e1cc2b`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 239.1 KB (239055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3479d262aebc44602af32ef7336be8974c16ae723c6ab77fba1e7f9149483d`  
		Last Modified: Wed, 01 Feb 2023 18:49:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:91558095dc8910356f23d8076b9e5bf353defc04223d3ee7a18400505ca71261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:cada10ba69f57f775b9a16faf888565f07d1b296414c488e3fca9431c22eb82e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34455516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b792d6fc44f8bc39ec8ca5d656529a5b8e1492d6cf4d082b0cd49d8488881de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:59:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:59:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:59:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400062d61da6ac9d18eda99b4de78dbf1a9cea47ada42fb59417bd7d3940966f`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 3.8 MB (3766134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dda20f552df25b1a3c041dc92181af9b5119500b13a52cde52648c6017d94c`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f682ee0399a91bfe1c17e2e5ab2568e45560917037011fec50f7d71e38f73`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cac7bfc4ecfa33e13fd29c32d5dcca6e240446d22389f2b5f5acfa67a23ebd`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 258.4 KB (258366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4da522322b179b93738a554ff42291674f410633468302dd3d7bd78301252a47
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27e0b58fd465ae00b00a9699e5f6d77c96a7ad58c71aaba7095dc9079d9128a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:09:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:09:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:09:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c38043ccc25501401b9d77af23fd531bac15eb599f37aa73c2942390f0f89`  
		Last Modified: Tue, 31 Jan 2023 18:11:05 GMT  
		Size: 3.7 MB (3739627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80411de25d3f2eee928df25a78042197af878bcef13d3d216f05d002d204251a`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062cb70e52c57d65210d9b388e6d54a802a2fe89c07a377d86c4ef4502ff590`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b27a9557ed3f80818b8a9ec76450e885b5ffe64974f8eb88642d67dd3319fff`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 259.7 KB (259722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:ccb27ac7137a1b4182dd842114c37428a600b752e0a730e9c549e04c9532a2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:db0328bfc73471afc6ea3959e9064784e0dd65fb33221f8f8521acec39130003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34455776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b38aceba7f88d45ed89bf01fcb40220c82e24b6d334c9b0b89d08767fd5b80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:59:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:59:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:59:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400062d61da6ac9d18eda99b4de78dbf1a9cea47ada42fb59417bd7d3940966f`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 3.8 MB (3766134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dda20f552df25b1a3c041dc92181af9b5119500b13a52cde52648c6017d94c`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f682ee0399a91bfe1c17e2e5ab2568e45560917037011fec50f7d71e38f73`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cac7bfc4ecfa33e13fd29c32d5dcca6e240446d22389f2b5f5acfa67a23ebd`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 258.4 KB (258366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11ca7c2dee167ced8c8ec1ceff5bc630ac061bdd9f59ed00071722ab7e4070`  
		Last Modified: Tue, 31 Jan 2023 19:01:18 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5b770230161b71f7a2138e112d463c38b90dffd6594d2f302b7a18d1b4ec02ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f059c6b605395fae939c68fffd06ebbdf64ae2b55e1622515c21d759152063`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:09:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:09:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:09:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c38043ccc25501401b9d77af23fd531bac15eb599f37aa73c2942390f0f89`  
		Last Modified: Tue, 31 Jan 2023 18:11:05 GMT  
		Size: 3.7 MB (3739627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80411de25d3f2eee928df25a78042197af878bcef13d3d216f05d002d204251a`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062cb70e52c57d65210d9b388e6d54a802a2fe89c07a377d86c4ef4502ff590`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b27a9557ed3f80818b8a9ec76450e885b5ffe64974f8eb88642d67dd3319fff`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 259.7 KB (259722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03b38e66b4a534e50a16c431fd0aef94dc19cf45e0e60da70a12541a9870f1`  
		Last Modified: Tue, 31 Jan 2023 18:11:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:9dc880c2ce22a2f4c430a893feafb23b00c13c743504b131c579fbe93c96be05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:f136bdf78d08ec8cf0feb11966e5587135c56e56e6f3905d0e5e674d5dffb6a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f359014092dda5786bb73d03ef8cad9f9d4ff58ea91dadffe2b00c30525e3606`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05cb95459d66a096424e07c1ed40a5be080386293e1f332d98587b154f495795
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65308759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1dfad29a96eb0452204b34a699e432f876d5238fc40e3091e78c5e88867c1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:051d60da7defa64efef48b78723ea65f7b1d4702e7a4ccd4e77ab5960eb3fe7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67612855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d387f73e7e78a2311817f3bb4aefe8ee66e61ed3db81bd4b1215fb7225919`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:a97711858e28814c8e2019e719ccda8933c91271dab31c2ccb4a122cb83f437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:6e4b662a92d3ec1149a040ad1a47e36b23a304c0026f1c6125c5a111ec14d792
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60971306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d0b9f65310222c90b6fd56e452fa4b774789baa56dacf1383695e4fcd3d520`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:42 GMT
ADD file:a2e9c6618e31202c1b929d106d9d8f2e98a0d6a45ae13b56e9149536eee01769 in / 
# Sat, 04 Feb 2023 06:52:43 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9338402809c6c0e98dbcb30453239ee887fa0b3378ee26565d576b66c08dfdea`  
		Last Modified: Sat, 04 Feb 2023 06:57:50 GMT  
		Size: 49.0 MB (49039305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dbacfb02619ae2748fd777216ca57eb38e5958cd05817de0397094f56ebb67`  
		Last Modified: Sat, 04 Feb 2023 09:51:24 GMT  
		Size: 11.6 MB (11649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7de9daa7ecef35d8e3cf7220527b1f3229fdd919fd1a88eab5c9c39c14b885`  
		Last Modified: Sat, 04 Feb 2023 09:51:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e71ee3cf5d725362eefcdd5f053e155b961b5711ab2a14608a8d76ce970798`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebce64a4f447022558af3e39249236b0fa69567c48b15ecd943ba9e02d824b`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6eb274643631939f13097c755fe3b8cf92bd7086309a009a638fbe6cd4c943a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60961349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d679ee54e61884acbc26f2ffce51aa67f4d41315ba0d0987a72d5f37fe00d5a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:18 GMT
ADD file:e0f39d8fee93f482160beca25b949b1de50ecc55ac86b1c276bed0b5c9955393 in / 
# Sat, 04 Feb 2023 06:18:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:541de84dec560e0a7dc13f9e5246f1a165b0955a6aefdc92d0bc46a50138a249`  
		Last Modified: Sat, 04 Feb 2023 06:22:53 GMT  
		Size: 49.1 MB (49064951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef954a467cdbd9442f76eae26dcce65b43e942cf51fb0fc9932a2ce11a37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:11 GMT  
		Size: 11.6 MB (11613149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb0ddc7c21670259cb7fa6d33e4a66293440c6bb9ac9b12014f6ad578ba76`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3ab955b5154981b3ebc74d79cacb2c050f8b3045d9e3b9bb5d5b3c6d69a3a`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e036d4fa82c2440e6b7a89404b4a9cdf679911cccfc91b67183e47fac4bfe42`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 281.2 KB (281241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:05801a70afb52784ce53c6a8349a412b3b66ea7cd6450e28751d608abc89936f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62071387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34563ef514aae65cb71b498e5aee43cd202ee94071b3dbfbd4f5d88c08704a88`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:50:25 GMT
ADD file:e52d2501a6498b9d4b4b7c45345d2dd2f2fbfa7df2849d1f794768270c0971a5 in / 
# Sat, 04 Feb 2023 07:50:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:18:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:18:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc17d0499e93f237d6be86c3138e9cea4fd1d950920edfec3d640e8d8b6e6230`  
		Last Modified: Sat, 04 Feb 2023 07:56:51 GMT  
		Size: 50.1 MB (50095432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656fbc116e7839c44add365bae3bd4349d21d05d7b091ea4d2098e710f66b512`  
		Last Modified: Sat, 04 Feb 2023 10:20:31 GMT  
		Size: 11.9 MB (11882314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb95e1e52ca35e75a37712cbc5eb1873f15267dec919dd455270db0a0f23b8`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a639ad9981483ad2e7134d897588b58d1ae44602db925d37a3df4025cbe07`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa136b4bccdbd7b70f5d182c78e89a19c4e9913b13cea10f72535f20aa0e3e`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 91.7 KB (91654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d2853d988feabf7b38fafbed14a52b7cd5b4cf0a7185d34f416c17870c906c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d9da91cb3a9f07c8da425c7cda24799df726d94aa9eb22e4514172aa4c932ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60971700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4695c4028d7039b105e47bfa3cc8ce9dc902a609c9256f299e0ae37dbe6ea4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:42 GMT
ADD file:a2e9c6618e31202c1b929d106d9d8f2e98a0d6a45ae13b56e9149536eee01769 in / 
# Sat, 04 Feb 2023 06:52:43 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9338402809c6c0e98dbcb30453239ee887fa0b3378ee26565d576b66c08dfdea`  
		Last Modified: Sat, 04 Feb 2023 06:57:50 GMT  
		Size: 49.0 MB (49039305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dbacfb02619ae2748fd777216ca57eb38e5958cd05817de0397094f56ebb67`  
		Last Modified: Sat, 04 Feb 2023 09:51:24 GMT  
		Size: 11.6 MB (11649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7de9daa7ecef35d8e3cf7220527b1f3229fdd919fd1a88eab5c9c39c14b885`  
		Last Modified: Sat, 04 Feb 2023 09:51:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e71ee3cf5d725362eefcdd5f053e155b961b5711ab2a14608a8d76ce970798`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebce64a4f447022558af3e39249236b0fa69567c48b15ecd943ba9e02d824b`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6174d2bb6eaf520ae243de994338976e5cf76d909ba7dbfe4b4c6593857ca1`  
		Last Modified: Sat, 04 Feb 2023 09:51:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dfc6d72a79ebae3679ff6b7311d814ad650c536b908466f05bfedab09c0c447
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60961744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8d4407ad794329f99fbc45860becd38ed0ebb95f343004673e640cc94f0e34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:18 GMT
ADD file:e0f39d8fee93f482160beca25b949b1de50ecc55ac86b1c276bed0b5c9955393 in / 
# Sat, 04 Feb 2023 06:18:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:541de84dec560e0a7dc13f9e5246f1a165b0955a6aefdc92d0bc46a50138a249`  
		Last Modified: Sat, 04 Feb 2023 06:22:53 GMT  
		Size: 49.1 MB (49064951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef954a467cdbd9442f76eae26dcce65b43e942cf51fb0fc9932a2ce11a37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:11 GMT  
		Size: 11.6 MB (11613149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb0ddc7c21670259cb7fa6d33e4a66293440c6bb9ac9b12014f6ad578ba76`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3ab955b5154981b3ebc74d79cacb2c050f8b3045d9e3b9bb5d5b3c6d69a3a`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e036d4fa82c2440e6b7a89404b4a9cdf679911cccfc91b67183e47fac4bfe42`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 281.2 KB (281241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69955de265518b9a0350d0446a8659f1d17fbd7262785ae52dae2c7b501b6e42`  
		Last Modified: Sat, 04 Feb 2023 08:51:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:16c8d81d15b568e86d9af3adb0b43b0045b75e3802336254f7698eb580837343
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62071782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4acac41d564ed2278b89367728dae97579fd7cf11a1596bab17e37c117107d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:50:25 GMT
ADD file:e52d2501a6498b9d4b4b7c45345d2dd2f2fbfa7df2849d1f794768270c0971a5 in / 
# Sat, 04 Feb 2023 07:50:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:18:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:18:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dc17d0499e93f237d6be86c3138e9cea4fd1d950920edfec3d640e8d8b6e6230`  
		Last Modified: Sat, 04 Feb 2023 07:56:51 GMT  
		Size: 50.1 MB (50095432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656fbc116e7839c44add365bae3bd4349d21d05d7b091ea4d2098e710f66b512`  
		Last Modified: Sat, 04 Feb 2023 10:20:31 GMT  
		Size: 11.9 MB (11882314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb95e1e52ca35e75a37712cbc5eb1873f15267dec919dd455270db0a0f23b8`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a639ad9981483ad2e7134d897588b58d1ae44602db925d37a3df4025cbe07`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa136b4bccdbd7b70f5d182c78e89a19c4e9913b13cea10f72535f20aa0e3e`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 91.7 KB (91654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251101bfb24b59909f35cb1c42a6ff833e72f3fcdf46088571875c7b51a3f53b`  
		Last Modified: Sat, 04 Feb 2023 10:20:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:20b1e4b385c295908c70bbc044e5efe1e77b360ba4955716cada49d307f79677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:b8cec976c7ae22d7eb1de919a8d17dda0ebb47bfb23ddf37e495bea5f5cf5413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8664646e57311fbef0fcca2b8a240ef4551469837bab7b884ac53b773f6cce29`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:48:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2c6114af2471df54db6a6f68996f51e5c6725dc13cd50218152e6b734fc9d`  
		Last Modified: Sat, 04 Feb 2023 09:50:29 GMT  
		Size: 10.5 MB (10504469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad61b917527e7bc9d3081b7d815d4312d7cd7b898cbb8a8a454c994afa032c`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894fb81d9c36b05fd865441fb72d450686bcabdd720cb053a0e26bfc4d172e9b`  
		Last Modified: Sat, 04 Feb 2023 09:50:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c75efa50c7d459603199041a9d1229bda46816a8c61d7e37754c14bf032d41`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 304.4 KB (304369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dc36f118472fb5e0b20c26b75d1bfbcf49480dfc7776c2e37ace4b31486be06d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f705abad5e5e4d726795ac15eae33baf5a4e1a515ff1054f4a3774e3fccc03fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda0b3f7673107c2204b83097e20a33728ef30d2e731e41727e0915eb8eb7c9`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 10.5 MB (10510366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e7e8e9562ff77a3d9a1bc9b20bcaaffb5ab25e375ce28460ba3a4018788fb`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c8ab4aac39ddf7a0f79a2cc135d4c299bb4a80b3282626e03ba7581e2ec733`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fc1d1a5e62555249343f0f0e4c5483c04f9b57bd28318895d6a9f14050a7e6`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 304.3 KB (304289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:e9ba4efba4fb4603470dfa4b361050c196a458e8db56b04b8482a6a5e3b49cba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61990982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef1323a087c0f2ec6cbfb43277e5eff5c495d0d796e6b0211e347ea7de54d8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b5157c7f1fe625aba139644ccc5d778bd2612aa09dbb07647cc8fb1645b7e2`  
		Last Modified: Sat, 04 Feb 2023 10:19:24 GMT  
		Size: 10.7 MB (10672599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c575c89dc25a96f058de33b540b31bcbcd0806e12baaa42524df5b83b25bb00`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549d3ced6edebcf3acdd958851b03298abe2d86782697f48fadf3ab90bd27f0`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4007a5e6d2ddd44a5c7d604ca425380f910138e3f9ccb53b3bb41818c2b57068`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 108.7 KB (108736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:5e21a5d696c2f24830b17ace2b22b92906df3aea7964965f403f18da363e180f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4eb056af4f99e5cf0e4bb36fb041598be17061b2f5badeb04de061d8a0d08e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65bb4c1dbc843123f57fbb6c227e448bf36bc91540efe30571d2e7373cd032`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:48:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2c6114af2471df54db6a6f68996f51e5c6725dc13cd50218152e6b734fc9d`  
		Last Modified: Sat, 04 Feb 2023 09:50:29 GMT  
		Size: 10.5 MB (10504469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad61b917527e7bc9d3081b7d815d4312d7cd7b898cbb8a8a454c994afa032c`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894fb81d9c36b05fd865441fb72d450686bcabdd720cb053a0e26bfc4d172e9b`  
		Last Modified: Sat, 04 Feb 2023 09:50:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c75efa50c7d459603199041a9d1229bda46816a8c61d7e37754c14bf032d41`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 304.4 KB (304369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d9bd0a1405d1b177e4fbba26da0f9cdde3947700b1810984c35e9b994dd984`  
		Last Modified: Sat, 04 Feb 2023 09:50:37 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9dbc4060d63354fc168ef4b4ce8d6572031d397dbd61b0240a71078697e7bc8d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e52ff1f01210e669f87eece484b274a1c9ed6dfe5aff7b6a0451113022b17b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda0b3f7673107c2204b83097e20a33728ef30d2e731e41727e0915eb8eb7c9`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 10.5 MB (10510366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e7e8e9562ff77a3d9a1bc9b20bcaaffb5ab25e375ce28460ba3a4018788fb`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c8ab4aac39ddf7a0f79a2cc135d4c299bb4a80b3282626e03ba7581e2ec733`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fc1d1a5e62555249343f0f0e4c5483c04f9b57bd28318895d6a9f14050a7e6`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 304.3 KB (304289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb106862c94d1d9cf42027a0b8de792e548f97d4bf206491e472fc6159c7e0e`  
		Last Modified: Sat, 04 Feb 2023 08:50:25 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6c16c1e38965d822f79bb63927ab57cf8eb2cbb537d907e84a89bbf24e1af8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2a0b1b021d82a33722be844bc6183dce33deab6f76ce2360e0f03a1e01fc2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b5157c7f1fe625aba139644ccc5d778bd2612aa09dbb07647cc8fb1645b7e2`  
		Last Modified: Sat, 04 Feb 2023 10:19:24 GMT  
		Size: 10.7 MB (10672599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c575c89dc25a96f058de33b540b31bcbcd0806e12baaa42524df5b83b25bb00`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549d3ced6edebcf3acdd958851b03298abe2d86782697f48fadf3ab90bd27f0`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4007a5e6d2ddd44a5c7d604ca425380f910138e3f9ccb53b3bb41818c2b57068`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 108.7 KB (108736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5f1cd364eb20620bd7ecfd8199b217eadb409140aa90a44a7e992a2c3e2c4`  
		Last Modified: Sat, 04 Feb 2023 10:19:33 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:9dc880c2ce22a2f4c430a893feafb23b00c13c743504b131c579fbe93c96be05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:f136bdf78d08ec8cf0feb11966e5587135c56e56e6f3905d0e5e674d5dffb6a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f359014092dda5786bb73d03ef8cad9f9d4ff58ea91dadffe2b00c30525e3606`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05cb95459d66a096424e07c1ed40a5be080386293e1f332d98587b154f495795
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65308759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1dfad29a96eb0452204b34a699e432f876d5238fc40e3091e78c5e88867c1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:051d60da7defa64efef48b78723ea65f7b1d4702e7a4ccd4e77ab5960eb3fe7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67612855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d387f73e7e78a2311817f3bb4aefe8ee66e61ed3db81bd4b1215fb7225919`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:08fcd85f86870ee5e676210963d6d22e463e4a7db52d874e14cfd62bda8d5f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c993c02f8bc36311ce8c06e0498a78563fd21b0d9363cdbaec2663151ded439d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4276a71ae9be81384cbfd82a8237629fc4ab2189d7a976fb15ea1650dcce2c6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3516a1ee8523855e4dad47eb62eb2523c08e5866d617bbfedb1b1189f1a8d5`  
		Last Modified: Sat, 04 Feb 2023 09:50:55 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30cf133c2939a3e22c8c9c47f8a7e66b7e2ff19edf863a0431e3912e80c6d7d0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65309119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a13b8f85eea85993fd122f87cf1d2e938e7897346d1e1ad5a275adf7ef906d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f08233a2e298109671c3c73b17ab2cadfcf1339e4cdf03e2f98d3c5f0bb5c7`  
		Last Modified: Sat, 04 Feb 2023 08:50:44 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:20e38f1a665337e410e5460f17d7289aa230f54fadb417fa78ce750a4d14ac08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67613214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c34efe9a2aa1e621ff74f9ebf3f4767bba6652c4007239b6aa8e8d3cea1ab7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7507e9bb7871aaa80f25eeb282f3810619c9d58c28a042a6045d823903047`  
		Last Modified: Sat, 04 Feb 2023 10:19:56 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:d8d24c7d181ae38e6555701a6b2fe2e267ca8aba201e3dc252bc95aeadbe68fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:cd16c6aef63a3db7fcb7cfbab5887e0f81e4803627f8f549d8e038cb3086180b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132d235ab4814815386bbcab148ddd5655f36d30392713c800468fedd7472205`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:50:57 GMT
ADD file:59c477049f0246331c6723687b7f8995e7a8946172b967d10fb8b67146220c33 in / 
# Sat, 04 Feb 2023 06:50:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20aeb9ca89f41415a92cd1a5e9ff6c0280e09a250e0f950c9df57d97b0d3efb5`  
		Last Modified: Sat, 04 Feb 2023 06:55:19 GMT  
		Size: 49.0 MB (49043016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b130d3ba13f067628bc387a54a1da8af7b4a096ce82ec156552956e406d7b`  
		Last Modified: Sat, 04 Feb 2023 09:51:06 GMT  
		Size: 11.6 MB (11649256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b839812e578b5131df5e1fedba0bac2db5b86c439d3b9d5f60c8acc2138048`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301743227e61250a633af79548b62dd2e3731aeff84a7ab7b0731685356d6b7`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348a923b18932afef779b25fb09416eeba581400fa1b039bbbfd9f718d400590`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 280.8 KB (280824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47d7a6535244ad6e95e521fd44c18618793ed1aa080c1eead00b9dcd26032188
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0990886517f471603003c7bff9a8442a9624b45903ac2c0307fba5b87c4eaf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:08 GMT
ADD file:b40ad920bd7dd081e20adf36435db50381b9998a1de3d2eac6b2c45734ce60b3 in / 
# Sat, 04 Feb 2023 06:17:09 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a43b5d5927a7651097e784be4430a6ade09951f5b6879cd06b0f51fc7c4812af`  
		Last Modified: Sat, 04 Feb 2023 06:20:30 GMT  
		Size: 49.1 MB (49081538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178538c5bc5dcf98be54976e26e3643caa3a37f742386a75aeeda9818488236`  
		Last Modified: Sat, 04 Feb 2023 08:50:55 GMT  
		Size: 11.6 MB (11613318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946ba90fc15d686558f937d9db8c112910bfcc60659eae41906cab00536fbd1`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d06715673a85e222fe91b40adfd40e6cf12abad4d8fc6b94aa1a329f289b576`  
		Last Modified: Sat, 04 Feb 2023 08:50:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b2fd07b19b38ae39db22c7c35d3f8f01c22b33486483bc0f26dd2f8d1e600`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 281.2 KB (281229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:af1f08b15a4552a4640cc28b82c5191420f39a7e659135c335e428b94832823d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62069539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb9530c0e32632a30dbc1f4c5c64f3550af137d440eb9d9dc1049930dbbae9d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:48:40 GMT
ADD file:71f93fd08314b2207fb2e5840185c4db4279fa8f008742cf35eaf4daf925d475 in / 
# Sat, 04 Feb 2023 07:48:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b6e1871a6864b2026696c7ffe48da3030a97146a6a0f3ca18f87c19b1ed6e05`  
		Last Modified: Sat, 04 Feb 2023 07:53:55 GMT  
		Size: 50.1 MB (50093420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e4ba6446be2b949171fc2868a8c59235d2af1758d013151fcd57d081401b6`  
		Last Modified: Sat, 04 Feb 2023 10:20:10 GMT  
		Size: 11.9 MB (11882451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70715b74ec52eab8e28b9acfabf935edf643321adb523d3d69a98e9486900a52`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdff03b60b1edaee34f47a2f80a061b637fca4ae130e5261d8d7f7ced5c14b10`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24bbda6354a4d781c58506977ac567ec1b139d570de8854e2130234b8d3a3c1`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 91.7 KB (91680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:ec2e654afac39e54093ddc4ddacd1cafc57d08a81e85cbe42849140f172c5010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:038d27cd30b1fbc077e69ef71a2d03e5754e5d92cc86b17c271c0912c0952c1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9217cccc9e4b0cb5b096d954ca7a60e94975fa1f08693781a8f53d48e5fd908b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:50:57 GMT
ADD file:59c477049f0246331c6723687b7f8995e7a8946172b967d10fb8b67146220c33 in / 
# Sat, 04 Feb 2023 06:50:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:20aeb9ca89f41415a92cd1a5e9ff6c0280e09a250e0f950c9df57d97b0d3efb5`  
		Last Modified: Sat, 04 Feb 2023 06:55:19 GMT  
		Size: 49.0 MB (49043016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b130d3ba13f067628bc387a54a1da8af7b4a096ce82ec156552956e406d7b`  
		Last Modified: Sat, 04 Feb 2023 09:51:06 GMT  
		Size: 11.6 MB (11649256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b839812e578b5131df5e1fedba0bac2db5b86c439d3b9d5f60c8acc2138048`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301743227e61250a633af79548b62dd2e3731aeff84a7ab7b0731685356d6b7`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348a923b18932afef779b25fb09416eeba581400fa1b039bbbfd9f718d400590`  
		Last Modified: Sat, 04 Feb 2023 09:51:05 GMT  
		Size: 280.8 KB (280824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd55eff8502d8c054050f00e802fa327dccdd4b4c08c28c44be57867702d11`  
		Last Modified: Sat, 04 Feb 2023 09:51:15 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d38cc525233e026ed1dc6ab33d626e38579465070da1b007a4377ad7e892c38
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f457705f06d5d27f6710a5d2077f18bec766f68fff56c944f7ad6428fca9b65`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:08 GMT
ADD file:b40ad920bd7dd081e20adf36435db50381b9998a1de3d2eac6b2c45734ce60b3 in / 
# Sat, 04 Feb 2023 06:17:09 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a43b5d5927a7651097e784be4430a6ade09951f5b6879cd06b0f51fc7c4812af`  
		Last Modified: Sat, 04 Feb 2023 06:20:30 GMT  
		Size: 49.1 MB (49081538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178538c5bc5dcf98be54976e26e3643caa3a37f742386a75aeeda9818488236`  
		Last Modified: Sat, 04 Feb 2023 08:50:55 GMT  
		Size: 11.6 MB (11613318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946ba90fc15d686558f937d9db8c112910bfcc60659eae41906cab00536fbd1`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d06715673a85e222fe91b40adfd40e6cf12abad4d8fc6b94aa1a329f289b576`  
		Last Modified: Sat, 04 Feb 2023 08:50:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b2fd07b19b38ae39db22c7c35d3f8f01c22b33486483bc0f26dd2f8d1e600`  
		Last Modified: Sat, 04 Feb 2023 08:50:54 GMT  
		Size: 281.2 KB (281229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596e70a3c681969a418f4e81170b181a23350b8e71edecd45c416d7c429c37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:02 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f17948d0f4324a8463f4b46218f398ed9999a1286d1cd6a22634242bf24b268a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62069966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc12f02cb74b2e26e73e18689145b654a7cf1dc1e565925d1a7ff9962936f8f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:48:40 GMT
ADD file:71f93fd08314b2207fb2e5840185c4db4279fa8f008742cf35eaf4daf925d475 in / 
# Sat, 04 Feb 2023 07:48:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0b6e1871a6864b2026696c7ffe48da3030a97146a6a0f3ca18f87c19b1ed6e05`  
		Last Modified: Sat, 04 Feb 2023 07:53:55 GMT  
		Size: 50.1 MB (50093420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e4ba6446be2b949171fc2868a8c59235d2af1758d013151fcd57d081401b6`  
		Last Modified: Sat, 04 Feb 2023 10:20:10 GMT  
		Size: 11.9 MB (11882451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70715b74ec52eab8e28b9acfabf935edf643321adb523d3d69a98e9486900a52`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdff03b60b1edaee34f47a2f80a061b637fca4ae130e5261d8d7f7ced5c14b10`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24bbda6354a4d781c58506977ac567ec1b139d570de8854e2130234b8d3a3c1`  
		Last Modified: Sat, 04 Feb 2023 10:20:09 GMT  
		Size: 91.7 KB (91680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18447a03ec0fb4ac174af8327d90f68ad4c4aeca490e18fc4e4aa1d779098d8d`  
		Last Modified: Sat, 04 Feb 2023 10:20:20 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:e513ac1e11156aecac472db495f4a8a9289c483b45d0dc1b4a246b58da08ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:9eaae57e6a418b8c573fc5418ad64fe129309c35c2fd161bbdbf61a529730d9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31775229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873262071297edd49a7d33afe192f7dd416fbcb8f8329bfc9d17b220889f04e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:58:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:58:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:58:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c561dd565402593670454bc67f0d32877f005872b8d25d4a588ff0bd84d74582`  
		Last Modified: Tue, 31 Jan 2023 19:00:39 GMT  
		Size: 4.8 MB (4821347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199a21fc88a38a5953a4eda7d548104c2153dbacdbeac0c1f97636aa990429d`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4dc3134d8a8ba0f045aa233e851c13346eb4ea771d8394c56cf2863567c2a8`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c014dbfdfc0e1f416ac41d8cf451e1463598f92d704b7440a38610c18f4ebe26`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 240.4 KB (240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5683ede91c2464e5b6ae9098e6c50ff505d17f1fa2f3e71b42ead7b3feccd26f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490edb93bb34812d94fffb01906d7d28c3e9fc0bb12c7cd49c911c949fa7ad3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:08:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:08:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:08:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbc19e87e6da7df7a26b73c38813e606d157ff82cead74668aa9fb1dde50fe`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 4.4 MB (4403764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13f880e3b2e22e0f79bd577aae93628955db5dfb54dc16b5ee01d78e283612`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1536cf9d0676d119194aaac6a84cfd3883f661525fc07c8c16507232e4b0820`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d9d3933a870d2b232e0931a36cc44e9dc946dd9f6dcdb07cc55b77f21a170`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 241.1 KB (241081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:691ca2cf102d15603a0c797e930a351ed9c873489a8ee27f1e76b43eadc33e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7c10782a79f7c72117a5374ce52548ca719f89305356417c7957eef4ce83a492
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31775483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6c7baace0050bff9e555573db23e79cca0226c59505907eb177d7fd551e1e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:58:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:58:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:58:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:58:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c561dd565402593670454bc67f0d32877f005872b8d25d4a588ff0bd84d74582`  
		Last Modified: Tue, 31 Jan 2023 19:00:39 GMT  
		Size: 4.8 MB (4821347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199a21fc88a38a5953a4eda7d548104c2153dbacdbeac0c1f97636aa990429d`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4dc3134d8a8ba0f045aa233e851c13346eb4ea771d8394c56cf2863567c2a8`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c014dbfdfc0e1f416ac41d8cf451e1463598f92d704b7440a38610c18f4ebe26`  
		Last Modified: Tue, 31 Jan 2023 19:00:38 GMT  
		Size: 240.4 KB (240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb917c28cea7ae4fa4a9d361cbbd4494ecd182af107d7ee5936bcb018641040`  
		Last Modified: Tue, 31 Jan 2023 19:00:46 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0106f5e71d6be760cf4fa278aa89bf7ab086e4711f5751e8c9e46031e939ba69
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28382540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15489cd4bee72086827d309d7fa524ab5f75084ac3a273f752ba9de140d3d70f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:08:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:08:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:08:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:08:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbc19e87e6da7df7a26b73c38813e606d157ff82cead74668aa9fb1dde50fe`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 4.4 MB (4403764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13f880e3b2e22e0f79bd577aae93628955db5dfb54dc16b5ee01d78e283612`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1536cf9d0676d119194aaac6a84cfd3883f661525fc07c8c16507232e4b0820`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455d9d3933a870d2b232e0931a36cc44e9dc946dd9f6dcdb07cc55b77f21a170`  
		Last Modified: Tue, 31 Jan 2023 18:10:28 GMT  
		Size: 241.1 KB (241081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3633341f6970cb9798062d7a3e8b9c338cf172ef3b05cdc69e65ba08a562aee`  
		Last Modified: Tue, 31 Jan 2023 18:10:39 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:fc0e3f6a31571b6faef75452e7b452d8bd6b64ec637462b7dc067544e4285a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:85b798bdb26eb6b1340fbc60fc0feec533e7dd20029f088b82cb4839a401cac5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbceb465a22ad0be1c177c9fe16c5812526ba3dac6c3065f5eefbdd9efacfc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:32:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 19:32:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 19:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340633481010cfb4323a6980ddc3fbb99c2b231c2bae539ce3adbe4323848f34`  
		Last Modified: Wed, 01 Feb 2023 19:33:24 GMT  
		Size: 5.5 MB (5494456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a75d823acce0fa96f4fa88a59f0531577b8f2838bfe342fd493d768cbfcd`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1424e1c74c34cfbb9d0566bfa17947ded4bdff35d712e953ebe4b9a83f3483`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b985a598f6b1f9e18c76e8ff8ec2a3031cee1c84d02604bcde89fe5b75df28e4`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 238.9 KB (238907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f43cd8b79163c0d9d100aaf36b45be3a012257ff691d14de42300c681ff6862
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32909337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde545e728f21aeef32f65cf9201e112821ed623b0cd56fa89b9b5024752244`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:48:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 18:48:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 18:48:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5c02fa6b59ab2149fa6bd73b93cc90d70885b4c89395e276408e863c13469`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 5.5 MB (5474533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558f1a74caa43afa1ef7b67ba9f69563ea68ccc494931e60f17601e0d197766f`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc55772b4b9049168de57f770b06cdc6b133aad697a9d81fd887d0845d6b2e4`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64d2353b0251a8e328c31de617a38bc62b5f305270c4e614d42af92b1e1cc2b`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 239.1 KB (239055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:d60d4892922515af262d9b747b2b0c64622190e73ac678135285993f68ac0b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:168dd889aecd1f1d598a9b69160fa460d720c310f55b50eb7f132e76a28326b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7515b917b364356f96522dc926c5c828a4bf0df70fcf3945bd0f22f7fb7ba0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:32:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 19:32:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 19:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:32:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340633481010cfb4323a6980ddc3fbb99c2b231c2bae539ce3adbe4323848f34`  
		Last Modified: Wed, 01 Feb 2023 19:33:24 GMT  
		Size: 5.5 MB (5494456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a75d823acce0fa96f4fa88a59f0531577b8f2838bfe342fd493d768cbfcd`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1424e1c74c34cfbb9d0566bfa17947ded4bdff35d712e953ebe4b9a83f3483`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b985a598f6b1f9e18c76e8ff8ec2a3031cee1c84d02604bcde89fe5b75df28e4`  
		Last Modified: Wed, 01 Feb 2023 19:33:23 GMT  
		Size: 238.9 KB (238907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dbb4dc6c7f0965eb4d15b6c9b5762a70d0caf0e9fca5b9eb8c5dbe3211b746`  
		Last Modified: Wed, 01 Feb 2023 19:33:31 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:757707483fe2ff4d1589194906a99b162fc40a8b19fe18f56b7e989510aae4c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32909592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e032ef358f0f25a08aba8f3214453113a399a57680920f1d06b130156139f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:48:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Feb 2023 18:48:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Feb 2023 18:48:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:48:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5c02fa6b59ab2149fa6bd73b93cc90d70885b4c89395e276408e863c13469`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 5.5 MB (5474533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558f1a74caa43afa1ef7b67ba9f69563ea68ccc494931e60f17601e0d197766f`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc55772b4b9049168de57f770b06cdc6b133aad697a9d81fd887d0845d6b2e4`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64d2353b0251a8e328c31de617a38bc62b5f305270c4e614d42af92b1e1cc2b`  
		Last Modified: Wed, 01 Feb 2023 18:49:45 GMT  
		Size: 239.1 KB (239055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3479d262aebc44602af32ef7336be8974c16ae723c6ab77fba1e7f9149483d`  
		Last Modified: Wed, 01 Feb 2023 18:49:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:91558095dc8910356f23d8076b9e5bf353defc04223d3ee7a18400505ca71261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:cada10ba69f57f775b9a16faf888565f07d1b296414c488e3fca9431c22eb82e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34455516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b792d6fc44f8bc39ec8ca5d656529a5b8e1492d6cf4d082b0cd49d8488881de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:59:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:59:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:59:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400062d61da6ac9d18eda99b4de78dbf1a9cea47ada42fb59417bd7d3940966f`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 3.8 MB (3766134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dda20f552df25b1a3c041dc92181af9b5119500b13a52cde52648c6017d94c`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f682ee0399a91bfe1c17e2e5ab2568e45560917037011fec50f7d71e38f73`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cac7bfc4ecfa33e13fd29c32d5dcca6e240446d22389f2b5f5acfa67a23ebd`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 258.4 KB (258366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4da522322b179b93738a554ff42291674f410633468302dd3d7bd78301252a47
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27e0b58fd465ae00b00a9699e5f6d77c96a7ad58c71aaba7095dc9079d9128a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:09:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:09:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:09:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c38043ccc25501401b9d77af23fd531bac15eb599f37aa73c2942390f0f89`  
		Last Modified: Tue, 31 Jan 2023 18:11:05 GMT  
		Size: 3.7 MB (3739627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80411de25d3f2eee928df25a78042197af878bcef13d3d216f05d002d204251a`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062cb70e52c57d65210d9b388e6d54a802a2fe89c07a377d86c4ef4502ff590`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b27a9557ed3f80818b8a9ec76450e885b5ffe64974f8eb88642d67dd3319fff`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 259.7 KB (259722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:ccb27ac7137a1b4182dd842114c37428a600b752e0a730e9c549e04c9532a2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:db0328bfc73471afc6ea3959e9064784e0dd65fb33221f8f8521acec39130003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34455776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b38aceba7f88d45ed89bf01fcb40220c82e24b6d334c9b0b89d08767fd5b80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:59:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:59:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:59:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400062d61da6ac9d18eda99b4de78dbf1a9cea47ada42fb59417bd7d3940966f`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 3.8 MB (3766134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dda20f552df25b1a3c041dc92181af9b5119500b13a52cde52648c6017d94c`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f682ee0399a91bfe1c17e2e5ab2568e45560917037011fec50f7d71e38f73`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cac7bfc4ecfa33e13fd29c32d5dcca6e240446d22389f2b5f5acfa67a23ebd`  
		Last Modified: Tue, 31 Jan 2023 19:01:10 GMT  
		Size: 258.4 KB (258366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11ca7c2dee167ced8c8ec1ceff5bc630ac061bdd9f59ed00071722ab7e4070`  
		Last Modified: Tue, 31 Jan 2023 19:01:18 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5b770230161b71f7a2138e112d463c38b90dffd6594d2f302b7a18d1b4ec02ae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32386596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f059c6b605395fae939c68fffd06ebbdf64ae2b55e1622515c21d759152063`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:09:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Jan 2023 18:09:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Jan 2023 18:09:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:09:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c38043ccc25501401b9d77af23fd531bac15eb599f37aa73c2942390f0f89`  
		Last Modified: Tue, 31 Jan 2023 18:11:05 GMT  
		Size: 3.7 MB (3739627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80411de25d3f2eee928df25a78042197af878bcef13d3d216f05d002d204251a`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062cb70e52c57d65210d9b388e6d54a802a2fe89c07a377d86c4ef4502ff590`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b27a9557ed3f80818b8a9ec76450e885b5ffe64974f8eb88642d67dd3319fff`  
		Last Modified: Tue, 31 Jan 2023 18:11:04 GMT  
		Size: 259.7 KB (259722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03b38e66b4a534e50a16c431fd0aef94dc19cf45e0e60da70a12541a9870f1`  
		Last Modified: Tue, 31 Jan 2023 18:11:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:08fcd85f86870ee5e676210963d6d22e463e4a7db52d874e14cfd62bda8d5f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c993c02f8bc36311ce8c06e0498a78563fd21b0d9363cdbaec2663151ded439d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66650395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4276a71ae9be81384cbfd82a8237629fc4ab2189d7a976fb15ea1650dcce2c6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcc7194d0c4123d2cd826b5d6d00f8fe6a30bfa426f9dc4995c06f938be277`  
		Last Modified: Sat, 04 Feb 2023 09:50:46 GMT  
		Size: 11.3 MB (11310833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8c838289fc885f599f9b27e2e08431fbfadbf9811920752967dccbc4cd773`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662471f56650636c2c1a9a183fc6be2855acc9bb3497fcb75d639f7fde60d6`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fcb7e12dd89ae10f1967264cfb135cca0127ba2341900843a784c80f90643`  
		Last Modified: Sat, 04 Feb 2023 09:50:44 GMT  
		Size: 311.9 KB (311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3516a1ee8523855e4dad47eb62eb2523c08e5866d617bbfedb1b1189f1a8d5`  
		Last Modified: Sat, 04 Feb 2023 09:50:55 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30cf133c2939a3e22c8c9c47f8a7e66b7e2ff19edf863a0431e3912e80c6d7d0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65309119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a13b8f85eea85993fd122f87cf1d2e938e7897346d1e1ad5a275adf7ef906d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386b993c0071d2bcf4a8f2250bfbd4fd50bcabb2d47b8fe81cff3ba3c954ad1b`  
		Last Modified: Sat, 04 Feb 2023 08:50:34 GMT  
		Size: 11.3 MB (11313033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5a3d24e8e01f6ab066d7fad4947aa0a7e70547302d3f7882dd82dda9907d2`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4cb9fd8e38b57d30b04e23a8206ec76f508811e129bc4ffda4c8a0febef933`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f1f5a7996bcea0a9b6a82d9b7384a62a8068b963ff9d707f0152657540088`  
		Last Modified: Sat, 04 Feb 2023 08:50:33 GMT  
		Size: 311.8 KB (311789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f08233a2e298109671c3c73b17ab2cadfcf1339e4cdf03e2f98d3c5f0bb5c7`  
		Last Modified: Sat, 04 Feb 2023 08:50:44 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:20e38f1a665337e410e5460f17d7289aa230f54fadb417fa78ce750a4d14ac08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67613214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c34efe9a2aa1e621ff74f9ebf3f4767bba6652c4007239b6aa8e8d3cea1ab7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a437294011cd6b5c68941f3a8b67a341bad0b3486f53ea21ff87f067a1ab0`  
		Last Modified: Sat, 04 Feb 2023 10:19:44 GMT  
		Size: 11.5 MB (11500055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1266a8285fcad37334b09928ee9d8f26f56151d931cf79ca52eb8c0d2c55e7`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28de7c9af7430eef8d2c0febfb4470dbbd51227faeba47dd752dc71ef680299`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83d6cda1df334173912b00cf9c2ae3ee67b152962a769963483baf4e145273`  
		Last Modified: Sat, 04 Feb 2023 10:19:42 GMT  
		Size: 105.3 KB (105333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7507e9bb7871aaa80f25eeb282f3810619c9d58c28a042a6045d823903047`  
		Last Modified: Sat, 04 Feb 2023 10:19:56 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:a97711858e28814c8e2019e719ccda8933c91271dab31c2ccb4a122cb83f437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:6e4b662a92d3ec1149a040ad1a47e36b23a304c0026f1c6125c5a111ec14d792
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60971306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d0b9f65310222c90b6fd56e452fa4b774789baa56dacf1383695e4fcd3d520`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:42 GMT
ADD file:a2e9c6618e31202c1b929d106d9d8f2e98a0d6a45ae13b56e9149536eee01769 in / 
# Sat, 04 Feb 2023 06:52:43 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9338402809c6c0e98dbcb30453239ee887fa0b3378ee26565d576b66c08dfdea`  
		Last Modified: Sat, 04 Feb 2023 06:57:50 GMT  
		Size: 49.0 MB (49039305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dbacfb02619ae2748fd777216ca57eb38e5958cd05817de0397094f56ebb67`  
		Last Modified: Sat, 04 Feb 2023 09:51:24 GMT  
		Size: 11.6 MB (11649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7de9daa7ecef35d8e3cf7220527b1f3229fdd919fd1a88eab5c9c39c14b885`  
		Last Modified: Sat, 04 Feb 2023 09:51:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e71ee3cf5d725362eefcdd5f053e155b961b5711ab2a14608a8d76ce970798`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebce64a4f447022558af3e39249236b0fa69567c48b15ecd943ba9e02d824b`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6eb274643631939f13097c755fe3b8cf92bd7086309a009a638fbe6cd4c943a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60961349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d679ee54e61884acbc26f2ffce51aa67f4d41315ba0d0987a72d5f37fe00d5a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:18 GMT
ADD file:e0f39d8fee93f482160beca25b949b1de50ecc55ac86b1c276bed0b5c9955393 in / 
# Sat, 04 Feb 2023 06:18:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:541de84dec560e0a7dc13f9e5246f1a165b0955a6aefdc92d0bc46a50138a249`  
		Last Modified: Sat, 04 Feb 2023 06:22:53 GMT  
		Size: 49.1 MB (49064951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef954a467cdbd9442f76eae26dcce65b43e942cf51fb0fc9932a2ce11a37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:11 GMT  
		Size: 11.6 MB (11613149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb0ddc7c21670259cb7fa6d33e4a66293440c6bb9ac9b12014f6ad578ba76`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3ab955b5154981b3ebc74d79cacb2c050f8b3045d9e3b9bb5d5b3c6d69a3a`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e036d4fa82c2440e6b7a89404b4a9cdf679911cccfc91b67183e47fac4bfe42`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 281.2 KB (281241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:05801a70afb52784ce53c6a8349a412b3b66ea7cd6450e28751d608abc89936f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62071387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34563ef514aae65cb71b498e5aee43cd202ee94071b3dbfbd4f5d88c08704a88`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:50:25 GMT
ADD file:e52d2501a6498b9d4b4b7c45345d2dd2f2fbfa7df2849d1f794768270c0971a5 in / 
# Sat, 04 Feb 2023 07:50:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:18:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:18:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc17d0499e93f237d6be86c3138e9cea4fd1d950920edfec3d640e8d8b6e6230`  
		Last Modified: Sat, 04 Feb 2023 07:56:51 GMT  
		Size: 50.1 MB (50095432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656fbc116e7839c44add365bae3bd4349d21d05d7b091ea4d2098e710f66b512`  
		Last Modified: Sat, 04 Feb 2023 10:20:31 GMT  
		Size: 11.9 MB (11882314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb95e1e52ca35e75a37712cbc5eb1873f15267dec919dd455270db0a0f23b8`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a639ad9981483ad2e7134d897588b58d1ae44602db925d37a3df4025cbe07`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa136b4bccdbd7b70f5d182c78e89a19c4e9913b13cea10f72535f20aa0e3e`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 91.7 KB (91654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:d2853d988feabf7b38fafbed14a52b7cd5b4cf0a7185d34f416c17870c906c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d9da91cb3a9f07c8da425c7cda24799df726d94aa9eb22e4514172aa4c932ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60971700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4695c4028d7039b105e47bfa3cc8ce9dc902a609c9256f299e0ae37dbe6ea4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:42 GMT
ADD file:a2e9c6618e31202c1b929d106d9d8f2e98a0d6a45ae13b56e9149536eee01769 in / 
# Sat, 04 Feb 2023 06:52:43 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9338402809c6c0e98dbcb30453239ee887fa0b3378ee26565d576b66c08dfdea`  
		Last Modified: Sat, 04 Feb 2023 06:57:50 GMT  
		Size: 49.0 MB (49039305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dbacfb02619ae2748fd777216ca57eb38e5958cd05817de0397094f56ebb67`  
		Last Modified: Sat, 04 Feb 2023 09:51:24 GMT  
		Size: 11.6 MB (11649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7de9daa7ecef35d8e3cf7220527b1f3229fdd919fd1a88eab5c9c39c14b885`  
		Last Modified: Sat, 04 Feb 2023 09:51:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e71ee3cf5d725362eefcdd5f053e155b961b5711ab2a14608a8d76ce970798`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebce64a4f447022558af3e39249236b0fa69567c48b15ecd943ba9e02d824b`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6174d2bb6eaf520ae243de994338976e5cf76d909ba7dbfe4b4c6593857ca1`  
		Last Modified: Sat, 04 Feb 2023 09:51:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dfc6d72a79ebae3679ff6b7311d814ad650c536b908466f05bfedab09c0c447
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60961744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8d4407ad794329f99fbc45860becd38ed0ebb95f343004673e640cc94f0e34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:18 GMT
ADD file:e0f39d8fee93f482160beca25b949b1de50ecc55ac86b1c276bed0b5c9955393 in / 
# Sat, 04 Feb 2023 06:18:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:541de84dec560e0a7dc13f9e5246f1a165b0955a6aefdc92d0bc46a50138a249`  
		Last Modified: Sat, 04 Feb 2023 06:22:53 GMT  
		Size: 49.1 MB (49064951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef954a467cdbd9442f76eae26dcce65b43e942cf51fb0fc9932a2ce11a37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:11 GMT  
		Size: 11.6 MB (11613149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb0ddc7c21670259cb7fa6d33e4a66293440c6bb9ac9b12014f6ad578ba76`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3ab955b5154981b3ebc74d79cacb2c050f8b3045d9e3b9bb5d5b3c6d69a3a`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e036d4fa82c2440e6b7a89404b4a9cdf679911cccfc91b67183e47fac4bfe42`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 281.2 KB (281241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69955de265518b9a0350d0446a8659f1d17fbd7262785ae52dae2c7b501b6e42`  
		Last Modified: Sat, 04 Feb 2023 08:51:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:16c8d81d15b568e86d9af3adb0b43b0045b75e3802336254f7698eb580837343
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62071782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4acac41d564ed2278b89367728dae97579fd7cf11a1596bab17e37c117107d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:50:25 GMT
ADD file:e52d2501a6498b9d4b4b7c45345d2dd2f2fbfa7df2849d1f794768270c0971a5 in / 
# Sat, 04 Feb 2023 07:50:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:18:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:18:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dc17d0499e93f237d6be86c3138e9cea4fd1d950920edfec3d640e8d8b6e6230`  
		Last Modified: Sat, 04 Feb 2023 07:56:51 GMT  
		Size: 50.1 MB (50095432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656fbc116e7839c44add365bae3bd4349d21d05d7b091ea4d2098e710f66b512`  
		Last Modified: Sat, 04 Feb 2023 10:20:31 GMT  
		Size: 11.9 MB (11882314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb95e1e52ca35e75a37712cbc5eb1873f15267dec919dd455270db0a0f23b8`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a639ad9981483ad2e7134d897588b58d1ae44602db925d37a3df4025cbe07`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa136b4bccdbd7b70f5d182c78e89a19c4e9913b13cea10f72535f20aa0e3e`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 91.7 KB (91654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251101bfb24b59909f35cb1c42a6ff833e72f3fcdf46088571875c7b51a3f53b`  
		Last Modified: Sat, 04 Feb 2023 10:20:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
