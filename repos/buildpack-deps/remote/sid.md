## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:bbd4219c326ce61d29a98b9b325be6579bccb0fd2c10f2e4e8af1bd102887d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f7b11cf30bfc48da4d463bdbc7802a893e44044722e66534fc5cc55639d9318c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333891998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e63a204e4e71d7b4cf05c87c4a4c08cb51a4b5ed0adebeef87b521b6ed64c17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:44:37 GMT
ADD file:859abf2d579747b132742454ad96e32dc879955afff8af84fab63dc41312a0e0 in / 
# Wed, 20 Apr 2022 04:44:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:00:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:00:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 07:00:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:01:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:212be0dc3a8ffdc400158a5e3a9812f7413dbb5a86269ff50e41b84b37fdb9f7`  
		Last Modified: Wed, 20 Apr 2022 04:50:51 GMT  
		Size: 56.1 MB (56112566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b0603dc0dbc00177fa56a8c1af60fd29d0bf2e8e1e8df8772164b08d8ba1ac`  
		Last Modified: Wed, 20 Apr 2022 07:07:58 GMT  
		Size: 5.2 MB (5209066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da99ea31fc35c2341d30c71a1992c692753c04c61b2e1c25053bc3f9d269992`  
		Last Modified: Wed, 20 Apr 2022 07:07:59 GMT  
		Size: 10.9 MB (10924522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a400dfe0377271d31b8196be8ab40ac2db5aa00dd677d631d372b1df286ddb`  
		Last Modified: Wed, 20 Apr 2022 07:08:18 GMT  
		Size: 57.6 MB (57580832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e737e61d77637327f4941b94d43a2c816135ed42b06d67d0c7bebf76e8d7c1ef`  
		Last Modified: Wed, 20 Apr 2022 07:08:54 GMT  
		Size: 204.1 MB (204065012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fdf1c28f038cccf1d5a0174fd37efcd126cd1d56833939002f85ca04120ea3a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304914485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aff893dcacf1e388cf490e222e65942c354544f4f1fd9323f05f5a5187d99e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:20:15 GMT
ADD file:5cf288f7326d2adfff5d4d3ad0b8951ab86c23ab83cbd1d7799d5c3f7e16a857 in / 
# Wed, 20 Apr 2022 07:20:15 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:47:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 12:48:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:50:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8db2a46143e157b04953cf05194b0c408afa491a70876185538ed8dca91f9f55`  
		Last Modified: Wed, 20 Apr 2022 07:37:08 GMT  
		Size: 53.5 MB (53518487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341b88f54fc68d22e9e84a8661e65a14684ef134f7f3e5501db09108de37dcea`  
		Last Modified: Wed, 20 Apr 2022 13:07:30 GMT  
		Size: 5.1 MB (5105948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b40c86c120d43041e78ed7cce077bfa51b33140635f860a17b56fd9349f04`  
		Last Modified: Wed, 20 Apr 2022 13:07:32 GMT  
		Size: 10.6 MB (10597935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445e44e0b7b81da5c386d988323b74e27b2d376a346d93dee764c34c229b7cb8`  
		Last Modified: Wed, 20 Apr 2022 13:08:23 GMT  
		Size: 55.3 MB (55272800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c79d6d5afac61c34b0920099547e4905c97f3f5b7d4d9b25043c6ab7bf36cb`  
		Last Modified: Wed, 20 Apr 2022 13:10:23 GMT  
		Size: 180.4 MB (180419315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76158a26d7db0037ba3cf21e91ca684543726308a6262f36dc95c0f868c5c58e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291863155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babb37af268eebba6e553f44b78b0f329e5ed2302fd351aaa43e491b9fb81580`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:31:17 GMT
ADD file:0bbaf7ead1d59ceb682d490a4942a357b01272b17a3eb062c89673ee4e166052 in / 
# Wed, 20 Apr 2022 13:31:18 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 20:14:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:14:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 20:15:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:16:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2bdfb6c7c7f66a4f6d01a8add17283f952a25f6c31c2267fd53d1ff9148edc16`  
		Last Modified: Wed, 20 Apr 2022 13:48:09 GMT  
		Size: 51.1 MB (51125664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4823bde2923c5442c606b104de74dcb0814457fed2088fa724dd6831b9767bbf`  
		Last Modified: Wed, 20 Apr 2022 20:36:47 GMT  
		Size: 5.0 MB (4962895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767785c6f4268da31b8fbd1e7bd3fae5bfea9198e83ef63566d05d7bdce6428`  
		Last Modified: Wed, 20 Apr 2022 20:36:49 GMT  
		Size: 10.2 MB (10244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ed9c3ce00c659ad57fb1966e00c23737a28269aca3c7f45e75e5465b127332`  
		Last Modified: Wed, 20 Apr 2022 20:37:36 GMT  
		Size: 53.2 MB (53206444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4414c9734295b9af986849074417831c1c35fc543a7b82b37bfc713bacd80fb`  
		Last Modified: Wed, 20 Apr 2022 20:39:24 GMT  
		Size: 172.3 MB (172323471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7a4ab5d00cd6a37a9415a5f9c81b2a5241888511659640e39eec7494d2718b8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326533739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccae08ffc019d737fa3c47162910fbf8fb5e42e6b7d8eef14a62055658566bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:30:37 GMT
ADD file:21175f4b5f80ba5d755041ff362152a8991b53f89e3c6699275e0c99f6ff6acd in / 
# Wed, 20 Apr 2022 04:30:38 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:47:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 06:47:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:48:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:414d522b7454847f294a8c61536f57f36cb195df33ab1fce8c838de3d5ae109e`  
		Last Modified: Wed, 20 Apr 2022 04:38:18 GMT  
		Size: 55.1 MB (55063805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc9a9c4b1c386c65ac98874ab622afc88e90b73f7a0e1c692ab412bdd01c571`  
		Last Modified: Wed, 20 Apr 2022 06:56:31 GMT  
		Size: 5.2 MB (5195986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d918141859173a7d14691da560e5afcbb7c353d5694d9541d73f88867578c95`  
		Last Modified: Wed, 20 Apr 2022 06:56:32 GMT  
		Size: 10.7 MB (10691633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541426f7af00f836dff3b2b6976f4053e14eb4fe2fe3a8f804c6b8781c7c3fa0`  
		Last Modified: Wed, 20 Apr 2022 06:56:51 GMT  
		Size: 57.6 MB (57573714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2732c8da6e52e7d6997e689befeed4fa270a2cc129d2e72b58af2d7784e82c0`  
		Last Modified: Wed, 20 Apr 2022 06:57:27 GMT  
		Size: 198.0 MB (198008601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e5254477b171f67f5a20853e1c027dc470132bcf9dd036b26cd583da6bdc9de1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337035980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4969f7e766a7eaa63e9f2e360cb0efbd215ee73c13b3dadf6182edcec57f9d40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:39:08 GMT
ADD file:92a4df746589380f0ee875ec89574f67fa2f56164bbf20da79eaa902a778eff6 in / 
# Wed, 20 Apr 2022 07:39:09 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:20:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:20:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:21:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b42fb3c96c9db2aa67a5b3b033791b735ef01e8c8f15321f44a085532b703190`  
		Last Modified: Wed, 20 Apr 2022 07:47:30 GMT  
		Size: 57.2 MB (57154017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00924a45119800495fe2fa0b6d6aaf354e649da6676746c97c18df9c77e13002`  
		Last Modified: Wed, 20 Apr 2022 10:29:51 GMT  
		Size: 5.3 MB (5340392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faa8d253e5b8d891d6ce9b90e438656a4b5f68ca7b4dfb8f73c36b3da2e9043`  
		Last Modified: Wed, 20 Apr 2022 10:29:53 GMT  
		Size: 11.1 MB (11104264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f2bff506a180a1affdf12a35e0f3c11ba1731569fd21a8a49b19251f503f8a`  
		Last Modified: Wed, 20 Apr 2022 10:30:13 GMT  
		Size: 59.0 MB (59048052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7887396a007c5f2b272129a2ef5471999e838d476feae4f2ac7c8194131eaf06`  
		Last Modified: Wed, 20 Apr 2022 10:30:50 GMT  
		Size: 204.4 MB (204389255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:27a17385b3f17a4eb8247d14aa7b661afcde2156a36210edd575c2970fd44251
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314123434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f271efec93ca50de1effec31fe261475ed68483ad07aaadf833f388f4591386`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 14:31:30 GMT
ADD file:3ad0c34fcd14c5fe7c8ebdd604aaf6408b7bd1797df3867dc95c1e62649776f0 in / 
# Wed, 20 Apr 2022 14:31:34 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 23:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 23:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:38:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5f4c77aff8255984992f37180c0f928131e7372860c0f93b1c0b9320726de80d`  
		Last Modified: Wed, 20 Apr 2022 14:42:37 GMT  
		Size: 54.8 MB (54772282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89c264f04825b386c359d75b8413b57333d2dc19406b712e4d068e217c52bf8`  
		Last Modified: Wed, 20 Apr 2022 23:48:36 GMT  
		Size: 5.2 MB (5160621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3717b462f275ec8cc92879f116a0d1eb9a8d0edc5909c1aae7979d31243449fe`  
		Last Modified: Wed, 20 Apr 2022 23:48:38 GMT  
		Size: 10.7 MB (10673322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb29766e9c3cd0abcf658b8bfd96d7d63ea6a56b6844d0c07b603a763139d9a`  
		Last Modified: Wed, 20 Apr 2022 23:49:27 GMT  
		Size: 56.2 MB (56242479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7709b4c447708bec4844b0d01a9ebfe0a1b15248407da46fc21884ca1cf7c88`  
		Last Modified: Wed, 20 Apr 2022 23:51:33 GMT  
		Size: 187.3 MB (187274730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6da5284bfa9abf1159e70468a9c64c2d6d95c41bb4828cf04afc6b2d03f9287f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343997085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c367c207d37892993457a503bbaead322b83ade85e16069a4b4c5b2f0762bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 09:49:13 GMT
ADD file:fe481980541905937ff6238feab8ead20ee273dfc616bf9e647446ec0f98b510 in / 
# Wed, 20 Apr 2022 09:49:19 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:08:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 17:09:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:18:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a4e99688ea8909140343db9b1a83e87f7ddcee1e1ba6d630b79487e5e720199`  
		Last Modified: Wed, 20 Apr 2022 09:59:29 GMT  
		Size: 60.6 MB (60558000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9d38d0e81f1d25142863d436c077521a366a4b21640a92ac901895221e55ea`  
		Last Modified: Wed, 20 Apr 2022 17:34:37 GMT  
		Size: 5.5 MB (5483458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d48f909cc9d2e0af9952aff147f17b193c00be915fe067146c11dec81ebc29a`  
		Last Modified: Wed, 20 Apr 2022 17:34:36 GMT  
		Size: 11.7 MB (11703518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d315112327d37e1ce52ce2a20207b2e675c4977a693bb657bb705301a4348b`  
		Last Modified: Wed, 20 Apr 2022 17:35:57 GMT  
		Size: 62.3 MB (62263007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af38dda6c35baa1645b04390383620765fc87967dad639895a2d12b114a041cc`  
		Last Modified: Wed, 20 Apr 2022 17:38:03 GMT  
		Size: 204.0 MB (203989102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8eba6bd76e364d31f470138d12d10a3c1604ee5a3cef225f1a3f478f5abfc74c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342740508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a6357ff1e99d258d501d195f32663948044cc626d7fe2fa1ec67b1a910baae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:10:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e08edf3534b3a52b84e74759377bd253863a9cf43fa9dde36a31debd1990a`  
		Last Modified: Tue, 21 Dec 2021 03:42:27 GMT  
		Size: 223.0 MB (222972175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cae637d24f9ada05173ac2aa26d39f847aa7c80aaeba979a137c822d009198c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305932760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115dcf8948417886b0cde91cc10bacb2b52e0ae5e41d782e409b3125265ab2cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 08:42:10 GMT
ADD file:39be572f6c0b3f6f84497807d4bcb370f80b4ac4167f1857002b5571a4dba6b2 in / 
# Wed, 20 Apr 2022 08:42:16 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 11:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:21:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 11:21:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:23:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d9529e5f0bb592a3bb453a841aee9e6a765fede232bccdc538ec2c8b96421d2`  
		Last Modified: Wed, 20 Apr 2022 08:51:05 GMT  
		Size: 54.3 MB (54330969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8df2c317b7e7ca98f001f2d15c613527928de02e7eb3e9f728cd782b7338cf`  
		Last Modified: Wed, 20 Apr 2022 11:29:56 GMT  
		Size: 5.2 MB (5186233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e828f9d86f39827cc0435a54750db181b2f8df2785eca1dddfe35a5536c021f1`  
		Last Modified: Wed, 20 Apr 2022 11:29:56 GMT  
		Size: 10.8 MB (10818188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7992815e0e3b1d2397114927abda25dc906ea8fce59d9acb7a8cbb8c4c2e98`  
		Last Modified: Wed, 20 Apr 2022 11:30:11 GMT  
		Size: 56.9 MB (56898886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba5dedd264cf3486aabec961e86248ef0ece65693d91936f1d135d27e66e8cc`  
		Last Modified: Wed, 20 Apr 2022 11:30:39 GMT  
		Size: 178.7 MB (178698484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
