## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:01be24c10e4f726290c2dc70be0346896211ee962050f65415332526e2d88d6b
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f39d1309de0996b51a131440363ca2245aab2731cf7c9f03c5787c2a0d9e3054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 MB (346855572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595fe06196f67da1add2a8443bfd54f36eb73431f0e2f7e29339ffb019a9610f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:21:07 GMT
ADD file:0aaeb8a0c7fde9f030dc2ab67a03f21f44e9eecad9e4cf1f360dc5f768292460 in / 
# Tue, 12 Jul 2022 01:21:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:51:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:51:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:52:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a81bc091a3ce5ccc3c89ef56e710ee1854c5ff9fd3d7f148e87cb956b5b78c7`  
		Last Modified: Tue, 12 Jul 2022 01:26:19 GMT  
		Size: 53.2 MB (53226349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b567a2d645b715cf7eced5f75816db7c980c3416be39e599e6e4b0bbc82f9eb8`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 9.3 MB (9295637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303c4db152401668239f15446f8107b320fcfdc241030fd93f94783340b469ca`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 11.3 MB (11271765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf65a8772cd0616a80dfa0049c8ec6ea822121ccf534abed287a6206d6e1ca`  
		Last Modified: Tue, 12 Jul 2022 02:57:36 GMT  
		Size: 58.0 MB (57997898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e55056401bb9cc85acd66c40870e5f8399f7fb4815771ae89352591c3a642`  
		Last Modified: Tue, 12 Jul 2022 02:58:12 GMT  
		Size: 215.1 MB (215063923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ff2a232fc5e3b7a01e390d9f935b1069ebc17157f61aaf2c13862a22999f46f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.0 MB (505953641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166f5ef62281112b857a40ac40861b33d34bac092fe3cd2c0b3815f2bfc5f6ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:23 GMT
ADD file:2829a8dbc1e67454e67c0015efaaceadaa4b04330ed9e60cc8248246cac2aae2 in / 
# Tue, 02 Aug 2022 00:50:23 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:25:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:27:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11a67d4cf31e6e9dc8797a5c01d3198f326d91410c372d1a490bf5592578d9b1`  
		Last Modified: Tue, 02 Aug 2022 00:58:37 GMT  
		Size: 52.0 MB (52021372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6833771528bea1307d56591db306804d9768947a466a60b5de4f6b545ab0cec5`  
		Last Modified: Tue, 02 Aug 2022 01:33:35 GMT  
		Size: 8.7 MB (8741294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2288f8703c485a4ea82b9d9a1de8905ae4f0e420ca4f317625f441977a31c0`  
		Last Modified: Tue, 02 Aug 2022 01:33:34 GMT  
		Size: 10.9 MB (10946981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd5022e5328c139a6024dd9522e3ee6548067f8bf3200154271988ebb0457e`  
		Last Modified: Tue, 02 Aug 2022 01:34:01 GMT  
		Size: 55.4 MB (55387031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d8cee0d131bdd21a40fbaa40ccd4db499f48170c2f903c3dcd4f4179deb800`  
		Last Modified: Tue, 02 Aug 2022 01:36:50 GMT  
		Size: 378.9 MB (378856963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ab38321355c9474378fe74839a004aec7e04d37bf62f9f28ec9078ce78b6e890
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.5 MB (499495579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75640a6c12246fa07e428bf201ae76231bc439b9f207bbe46ad4675dd5bb41e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:02:35 GMT
ADD file:d11763b9aa59da9e9615c9a7df09de9c36f21a814e568fc0e11405310a9a2562 in / 
# Tue, 12 Jul 2022 01:02:36 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:31:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 28 Jul 2022 13:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:33:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce8fe2658d6ff3dea5d2d17cac5d8ea95c2ad6ebd5891a981d88d937403638c1`  
		Last Modified: Tue, 12 Jul 2022 01:15:55 GMT  
		Size: 48.8 MB (48767592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5060a56fd36f2eb179438d2b0be5a97d3620880188f3386a4a337bebedbf6488`  
		Last Modified: Thu, 28 Jul 2022 13:56:16 GMT  
		Size: 8.4 MB (8422217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc88f502700d322be499b780d0ac7619436180e0025b4181096a8bebc512379`  
		Last Modified: Thu, 28 Jul 2022 13:56:16 GMT  
		Size: 10.6 MB (10588874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2823b3b3de64aead8f8101b65c458017a4cdc468ce90501b9b3b31e2676ee5`  
		Last Modified: Thu, 28 Jul 2022 13:56:48 GMT  
		Size: 53.4 MB (53361588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd716377b61ac1ecbe6934b740e714151c5e1e3b10ee2a835e417366eb439adc`  
		Last Modified: Thu, 28 Jul 2022 13:58:47 GMT  
		Size: 378.4 MB (378355308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a99541e1fab2bae7405dc2fc47fd746b7ee1d601e7106c99e1171ef6e8f31244
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.4 MB (545357415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a535e1d2ed7d83864f1a6a75c3b3076b52759b90e3efafb766ab23e34eb571f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:477966410dd9e274b01740d7af857db5c024b4c4e53a5e83b5da6854d5b0c209 in / 
# Tue, 02 Aug 2022 00:41:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:27:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:28:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17bcb8e39c7f35480d4c2e5b46b6c0a58dac180206453cc49052707aa8053632`  
		Last Modified: Tue, 02 Aug 2022 00:48:00 GMT  
		Size: 53.3 MB (53311787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040e49dab65b12b89c427063ea6eec0802e14801664648c428e5a774754f3e73`  
		Last Modified: Tue, 02 Aug 2022 01:47:00 GMT  
		Size: 9.2 MB (9150009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b71a9f562c782f5916aedb7846293c7057b9f5f32ac072f785d2b21839f530`  
		Last Modified: Tue, 02 Aug 2022 01:46:57 GMT  
		Size: 11.1 MB (11062337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1205e62166cd9b96a2220ead9f68603c3996816c0b7e279fe1afb47d74ea5975`  
		Last Modified: Tue, 02 Aug 2022 01:47:20 GMT  
		Size: 57.7 MB (57709839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7ccfdc08190bdcc5d9a2f66cec9e502d18bcd6ee779573fbdbf2a77a75fc6`  
		Last Modified: Tue, 02 Aug 2022 01:48:30 GMT  
		Size: 414.1 MB (414123443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f315fd1c7be005e741f3142d28b7a76b094b3f9fb466467bd7523106160aa0e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348784110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbd3d4e07becebc4a5be20edad6f4002e78a2450ce2e3bebf4921406dd93c8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:23 GMT
ADD file:40a2042e14b22d803da216af628cd6e8603c923c4fe79ca3c4c79c95c1c1e878 in / 
# Tue, 02 Aug 2022 00:40:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:12:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:12:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:13:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:14:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef86b631f45587b4b6d1c16b80732997a4895ae8df072b14d68c25aeff8b901e`  
		Last Modified: Tue, 02 Aug 2022 00:47:20 GMT  
		Size: 54.2 MB (54195066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4385d16696693ee42b7a7f20009fa801f71ca0c6e014ce30f294f40d9993e965`  
		Last Modified: Tue, 02 Aug 2022 01:26:51 GMT  
		Size: 9.5 MB (9480230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed00b31a2aacbca3fdd1dfb26c6e14bf0bfbd4ab13f2498063fe7786ad715669`  
		Last Modified: Tue, 02 Aug 2022 01:26:50 GMT  
		Size: 11.5 MB (11473533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd03748d20b403da16ec2105506ec777552bb9d8960f48500514674a687d5b8`  
		Last Modified: Tue, 02 Aug 2022 01:27:13 GMT  
		Size: 59.1 MB (59113338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced0d92e73c4e80fee274f411add7132ee9cc8bf10f8928730af697d5c0cb6`  
		Last Modified: Tue, 02 Aug 2022 01:27:50 GMT  
		Size: 214.5 MB (214521943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4c8c18b9bd9d9d1339803a701905cf0afbbab16faec16da075aa35c99de3a541
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325729975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7961355c72646ef884f44ea9bc1b3c2550cfade043d1319df441d161fc778762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 04:44:00 GMT
ADD file:f6825f1dd59126d26ef0dba330a1d0eff37f6b9d56fe4a1bf2669774a6a7c74b in / 
# Tue, 12 Jul 2022 04:44:06 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:28:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 06:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:36:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:043042ab5eb51d2e5fe9f7bf85b86a91823ebf404e02b09bd9d96e29066acc7b`  
		Last Modified: Tue, 12 Jul 2022 04:54:59 GMT  
		Size: 52.3 MB (52346196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78102f519b643046757a9cd4f6d008518ddaf7e24f82322dba5336a7bff1dd7a`  
		Last Modified: Tue, 12 Jul 2022 06:46:55 GMT  
		Size: 8.7 MB (8664834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf3efe7ae97a67b5d9d9a2fd74d9d6407dc893ffcf6df03128e98d57bb34138`  
		Last Modified: Tue, 12 Jul 2022 06:46:55 GMT  
		Size: 11.0 MB (11033383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347923227ed46aa579c468e307ffc94f47c04832fca5d90d1787e75a20df5a5f`  
		Last Modified: Tue, 12 Jul 2022 06:47:47 GMT  
		Size: 56.7 MB (56694820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0598611b96746d3cf1760a3374380bf2db200b223feb7a7de3010b3bb5777ef`  
		Last Modified: Tue, 12 Jul 2022 06:50:00 GMT  
		Size: 197.0 MB (196990742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3a39dfe14be09b5601762c5ae7ceb7d9bde609b1b676a403fecc820de925f637
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.0 MB (562014957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3645747859a7f8685e45e2c9b325a7c4ac99c5945112a8eda240b7d5ecfabadb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:27:28 GMT
ADD file:8039654bddce2cd83d9433d1df0a53c329e7877cc8210593bcde23de63e2f1fd in / 
# Tue, 12 Jul 2022 01:27:36 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:49:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 22:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:53:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d4394941206b4f218ffa2a2b794698da5149ab7a22b52f71390aec65a7add3e`  
		Last Modified: Tue, 12 Jul 2022 01:40:47 GMT  
		Size: 57.4 MB (57441462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e13dc094f3be3cdae228630277f198c2aee4ccf4989e03df692829782575ad`  
		Last Modified: Tue, 26 Jul 2022 23:51:25 GMT  
		Size: 9.9 MB (9889588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148c549699d52333ba063274d8397af520c8317b8d893c23ba0800047eb2b45`  
		Last Modified: Tue, 26 Jul 2022 23:51:25 GMT  
		Size: 12.1 MB (12082932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c97a942b806632ce20c77655f33f494e860c5c99b3cbbe88c8a6d4a5eda5577`  
		Last Modified: Tue, 26 Jul 2022 23:51:54 GMT  
		Size: 62.3 MB (62265451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96183528d1d38b51d1dfeeb453517fec68f51cc929b0d9f3767b877fae0af8c`  
		Last Modified: Tue, 26 Jul 2022 23:53:41 GMT  
		Size: 420.3 MB (420335524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e46c8b614365372c5c9be7b6c96579d67afb902c84c6ecb2313fdd1cd7b43555
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.2 MB (353203662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5eb0b2811e65c3b1e7308c6ddbfa4e45657d8288257df0b82ed715e22caad0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:11:50 GMT
ADD file:e156d172727c94dd7b17970577469d9b556db67960762f454d5b90dad3f746bb in / 
# Thu, 23 Jun 2022 01:11:53 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:58:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:59:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 02:04:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:13:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70334332338a08f7ae515b43812936d5898e62e8ffd5fd38ba59761c5ed137d9`  
		Last Modified: Thu, 23 Jun 2022 01:30:12 GMT  
		Size: 49.4 MB (49429796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5fc26886e551b626bc82f99096f4659ee9ee5af689dad0d03fc75d88c37d88`  
		Last Modified: Thu, 23 Jun 2022 02:51:42 GMT  
		Size: 8.4 MB (8394795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6176147b43ca0f721514815cbe526cd0e19723ed30c23a9a3534a95d32d19cb`  
		Last Modified: Thu, 23 Jun 2022 02:51:43 GMT  
		Size: 10.7 MB (10650389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feebc8d66990654882c5fa423a1a4c713b77656fe3fb7540e4e51bbfcd8395d3`  
		Last Modified: Thu, 23 Jun 2022 02:54:14 GMT  
		Size: 53.9 MB (53944102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3867d2f4b79609cf8ab1715ce25955a2ae6c4b435db2275bd1962bb9969ee80e`  
		Last Modified: Thu, 23 Jun 2022 03:01:29 GMT  
		Size: 230.8 MB (230784580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5e5eb2e89ee6e720e75ca36a2281597de240ce21f5fb250d6f6a256010ea03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.5 MB (500475359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa54a4ef283eb54a28dd4bc552330112a16ce9eabe3b5915b94536263ff3032`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:43:36 GMT
ADD file:19dee33de85aac92620de3bd92768833a889db0b60b7445419bccb4285c46f94 in / 
# Tue, 02 Aug 2022 00:43:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:12:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:12:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:13:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31888e988211ae2cd4058438d0fd3d3420a26d35f21e97741527c1e85ad2d476`  
		Last Modified: Tue, 02 Aug 2022 00:49:29 GMT  
		Size: 51.7 MB (51734666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd60a4351ebe5fad9f32c09d0a6f7ec29b6c6dcb5ff8c29e6650149557447e2`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 9.0 MB (8960873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0db795ce4385e2a159326c7d9ab52e109942607b82b1c377894e874e601d`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 11.2 MB (11166864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891cb8548d01d5cd140a6d90fa3462f4433c9891f74f6d5405b9556edaca1a0`  
		Last Modified: Tue, 02 Aug 2022 01:37:13 GMT  
		Size: 56.9 MB (56935914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9889f124f3e95bd877e0a305131f335147bbe379811baf82c7a74227c39adac0`  
		Last Modified: Tue, 02 Aug 2022 01:38:00 GMT  
		Size: 371.7 MB (371677042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
