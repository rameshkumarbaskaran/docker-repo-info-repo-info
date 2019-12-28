## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:8d392166cddd49bce8f535d5baa380124810ce75f767664f33c7a89ded3fe551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1a03aa0d012064939b130972b0af8b8c92e56d8a348c5ac1312bdf1a4963a94b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321085419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26298bed7bb062bddc23ae8e3af026621813aeca9503e6f992be7eef3f3dd42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:47 GMT
ADD file:68b1541306250f957e5f1035d80f5683c1ed22e73cf2f2b563adc52424897a09 in / 
# Sat, 28 Dec 2019 04:22:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:57:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:57:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0b468739e287d7cd8fa8bcb34afb10216f12567d28caab345db8873c4246896`  
		Last Modified: Sat, 28 Dec 2019 04:27:19 GMT  
		Size: 51.5 MB (51479608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44261d6f427d89f764fcd9898d2845c7327812575dcc485436bb888b2ee1d0c7`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 7.9 MB (7919965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd42132ce8afeea96ec992f4170f1b4fe9fa1a621a93dc2d236088351e29685`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 10.2 MB (10183322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c16ba6f425320c83bd55536bb502f6e0b7064468bed05a5dcdbf0a13e9d892`  
		Last Modified: Sat, 28 Dec 2019 05:03:45 GMT  
		Size: 54.7 MB (54742028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a25030e962fd2e6934c589d89d5843df2d92e6833602ec2e97f45f5da0db86`  
		Last Modified: Sat, 28 Dec 2019 05:04:23 GMT  
		Size: 196.8 MB (196760496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea6a2e47f98763c80ea675f2b16dc3ee6d66463fb904c7c0e13780bb5a0f8a86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292413072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b925085df245a4d0fa1999764192eb38b1ea423f0e86cbb434c5e3c08d8012`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:51:51 GMT
ADD file:03cc60d1d72b99d3b1d122da1d59f729e29848dbbf6dd18cbf657a4c38ef0b5f in / 
# Sat, 28 Dec 2019 04:51:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:38:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:39:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:42:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:58904a701fa9ff155e476053cdd7da105682fd34a283dfecfc029765d82bc148`  
		Last Modified: Sat, 28 Dec 2019 04:58:52 GMT  
		Size: 49.5 MB (49475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8962cbd68da3db27dc20b92f9e448d10c3a6823e53156f2ba301e54789b010`  
		Last Modified: Sat, 28 Dec 2019 05:53:19 GMT  
		Size: 7.5 MB (7494157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f950a4075ac360274a49d98d4a4c73c351f221ac1f7acf157df1e1b62627fe`  
		Last Modified: Sat, 28 Dec 2019 05:53:20 GMT  
		Size: 9.9 MB (9877715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af595a9e5bd9d6de775039fb231e4cee16d03103b4186f91823002517a8cb892`  
		Last Modified: Sat, 28 Dec 2019 05:53:44 GMT  
		Size: 52.4 MB (52351988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7732540b0af215a51b95180392926051a8717e644edeeb3fbb4486911ddd78`  
		Last Modified: Sat, 28 Dec 2019 05:54:39 GMT  
		Size: 173.2 MB (173213221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9ba272b7640e3c65dd6564cd702fdd42f2a5f2868eed3bdc6bf56beb380c05b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286857569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954ff2810c81634d11e0f31ac9d18d80872e83a8dfadfef127c1ebf533ee5382`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:01:32 GMT
ADD file:b5c7da33763f5d6cace9605e53bf483375c1f792de0982f47885c85b47304392 in / 
# Sat, 28 Dec 2019 05:01:36 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:55:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:56:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:56:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:59:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d5856d0eb425d736e9f4c60a79333c1933bada38a126c109eff8f1eb43a9c21`  
		Last Modified: Sat, 28 Dec 2019 05:09:48 GMT  
		Size: 47.2 MB (47210722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3768cabb2504bdc0d3bf15c2e022ab2e94f61e198eb24b077cb6c5e620d5ac`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 7.2 MB (7234041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfad613eea011450300250c8f76f687229e6483a59e575849962e519e171c0b5`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 9.5 MB (9529582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdba93dc41685dd6b3cc9be45d32c5995478ce980c4972401e0c1b17f7c5c70`  
		Last Modified: Sat, 28 Dec 2019 07:10:09 GMT  
		Size: 50.2 MB (50193053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d048b5d0f9a0634b69822f8bf5830246aa1a01da6bf253b54f91502476b43fd`  
		Last Modified: Sat, 28 Dec 2019 07:10:55 GMT  
		Size: 172.7 MB (172690171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08e1db0748ae06f9422ca82b96cddd51864935f97b9d9807db95a5751f42784b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313004333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a2d4049a09f5ac3b65195411daed05d275b16d321fa64ff1eb2c21bccf5c3f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:03 GMT
ADD file:8932c68f3cf662412b086b3ca8b215a092fa5ea459074d42d359a9c778563152 in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:10:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:10:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:11:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:14:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:898762c0a5be611b2ded7eb33fffee89def5fd9c6161871b3f1f06e970b7739e`  
		Last Modified: Sat, 28 Dec 2019 04:47:51 GMT  
		Size: 50.4 MB (50431115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2023cefe917f460362808fc93a5f289f46561002704988023a04abcb63d8e`  
		Last Modified: Sat, 28 Dec 2019 06:22:45 GMT  
		Size: 7.8 MB (7795190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e6a5a666546a2fdc4d7d715747caa149ef9d403b43a49fea4ac6d10751a0ee`  
		Last Modified: Sat, 28 Dec 2019 06:22:45 GMT  
		Size: 10.2 MB (10192064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f57c50a4b46a7b065b414b42e8f96aeab062a797c90cd356311ed7956b2aad9`  
		Last Modified: Sat, 28 Dec 2019 06:23:10 GMT  
		Size: 54.9 MB (54938683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff11619a85b7863b887afc6d2be5fb4a1b3300554f0ab739b3a42c301e6fd9`  
		Last Modified: Sat, 28 Dec 2019 06:24:04 GMT  
		Size: 189.6 MB (189647281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:65dc09534fb5874b479da960a656f9f2d9b7ab56c971366cf93be7beceab6752
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330725579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57e65816f3eddb9c45f0369b716bc9cba743c4f35444784b20365e734760ad1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:02 GMT
ADD file:028a6b956388b2cf033fb64213fca841fe5708f01d7143a9883bb44273bfb987 in / 
# Sat, 28 Dec 2019 04:41:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:35:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:36:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:37:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b389037d8e8619e17e0b7de53ac2f84439d0b5b064350f604942c26d3b2f2608`  
		Last Modified: Sat, 28 Dec 2019 04:46:15 GMT  
		Size: 52.6 MB (52610734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9b069a84283b0c0d2f882f9d796b59f53ba2902179668ce465cd0e263633c8`  
		Last Modified: Sat, 28 Dec 2019 05:45:43 GMT  
		Size: 8.1 MB (8094045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474cbca8bafdcb28b1de38a11db97451990b86d610422bd137c2e7b61a86c3db`  
		Last Modified: Sat, 28 Dec 2019 05:45:43 GMT  
		Size: 10.5 MB (10534541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30619627ec66811f54c8f4675cbf7937aeec0c8ced378e14c6824f56ab9cb4d`  
		Last Modified: Sat, 28 Dec 2019 05:46:06 GMT  
		Size: 56.6 MB (56550490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc627985fa232511c27e0a717cdd9a740bf998f879d83534fccde5a8436d0e0`  
		Last Modified: Sat, 28 Dec 2019 05:46:58 GMT  
		Size: 202.9 MB (202935769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aedf50c27b844a2ea8f3929c62edf13328290b6cee67c99e2b1e0e1dcc22379f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340431991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ce59a61bd1a93d3993f1426ee5ad8a87ea08ede9aa4696a3aada493ef1f001`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:44 GMT
ADD file:d7ba1f92f51134645d0c28cccf74dc6cc9cff62c18d1e7ea24e9306b603cc4c6 in / 
# Sat, 28 Dec 2019 04:21:49 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:04:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:11:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a19f8e61b2d8b008c7115d66fcae892bce80e022931657219cecb2a15110c398`  
		Last Modified: Sat, 28 Dec 2019 04:29:56 GMT  
		Size: 55.3 MB (55284979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814b37b063181f0e69d2ffc211b88d130aa8935273a93f9155d2df7a1bf9c150`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 8.4 MB (8352650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1122a79a4397f123afc0998256257fa3fcdfa99567d9a6e43d19cdaac02f9ee`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 10.9 MB (10946018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501c344b50ae868e0144d013d546e02a4c4033ebe9c8fc067ee90f568efc396`  
		Last Modified: Sat, 28 Dec 2019 07:24:22 GMT  
		Size: 60.0 MB (60040117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bc72873e77d179d29fec41a6f95ed3cb89c5ec6bfc485bacb0f68449e78cb`  
		Last Modified: Sat, 28 Dec 2019 07:25:28 GMT  
		Size: 205.8 MB (205808227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:67b7ca4228dbb3ade38b603be9d7f2d7563da4caf763fd0744bc1e78230c5233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301606262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471198076e021f2e502bce9c0f612e463624f33bbdbd0dbc58bd19623f43dde`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:32 GMT
ADD file:ebe1df568622bb8e8e8e3b2318d11550389d84f3196d3ade9aaa9ecfdecd1028 in / 
# Sat, 28 Dec 2019 04:42:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:47:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:47:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:48:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:49:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d0208a582df93acf7a81d059abd969865a1e647765a53c87e2123fb6b283a34`  
		Last Modified: Sat, 28 Dec 2019 04:45:42 GMT  
		Size: 50.1 MB (50131585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46a42bc5c7805eb22e48c27565c0a108b60dd3c74386aea7cb2a2b367d00d07`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 7.6 MB (7591630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77c311db77933f5cbc7d2dc6e649e1d95c34ce4c806932601722b88f9b28a61`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 10.1 MB (10069342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc903c6290ae481b2ee639d7b0ce90ef144f5db8cf1c9f396e521df9b32214c8`  
		Last Modified: Sat, 28 Dec 2019 05:54:25 GMT  
		Size: 54.0 MB (53985858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe289d8445f03ea8910f2c2b83a54b83e51e04c3acb6514534b860fda702aee`  
		Last Modified: Sat, 28 Dec 2019 05:54:50 GMT  
		Size: 179.8 MB (179827847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
