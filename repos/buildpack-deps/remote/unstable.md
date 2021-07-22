## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:83c1e4f03210321d55d21c6ca2bbce6d4e5e067aef91e18cd4b73766a7b28ba7
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
$ docker pull buildpack-deps@sha256:57ff099db5a836305af9f98e362f8c67e57c2db5f731bfcc1081429efae2ba60
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322641075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41078bfb0eafd596305e9bfacce302fe23429cf77fd02ee6a68a02c5ede3d7b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:46:20 GMT
ADD file:cac9ad9d988141c80929e8c31f4cb388618dac0bbc048d4c5e3b8029c85c576d in / 
# Thu, 22 Jul 2021 00:46:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:13:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:13:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:531fc43e70accbfd0e52721b79cfd564769d6f1b7e64a98e9f670327d4c4820e`  
		Last Modified: Thu, 22 Jul 2021 00:51:36 GMT  
		Size: 54.9 MB (54909299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3334cfec756c2189b8a7cce5cd3ddf363b2acfc7b8a38f1ccf8cdbe4ef115`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 5.2 MB (5171133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284c0769674315a1486ea9eee2a7dbe2a630850d90b8e445a2b8d7034528be1b`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 10.9 MB (10872519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5845626ba0291c9852420419c76d5f8620b7801dc4b4420487f0119d42c59b6`  
		Last Modified: Thu, 22 Jul 2021 01:21:30 GMT  
		Size: 55.3 MB (55260477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217673b77d2543ba1967190c34c8c38cbcbe3ab6c8261c18a9e0483f5cf11b56`  
		Last Modified: Thu, 22 Jul 2021 01:22:09 GMT  
		Size: 196.4 MB (196427647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0a39be9471a03eccc10028eeb09228d696deb0f01fa8b4866cc5ee2d058a1a23
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295708002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9614a2c78488b157ccd0b39a2632a51befd1387bb0c58a05c34e592cf8355d77`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:51:25 GMT
ADD file:7b9b18b6a1a6deb81eb9bf8638d60de26198ba106aaa757dfb838b264fc90252 in / 
# Thu, 22 Jul 2021 00:51:26 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:07:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 02:08:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:10:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9de879dbb26d0cc624c499f5907a14117d0f357e4e39699d3208c57d5091b537`  
		Last Modified: Thu, 22 Jul 2021 01:04:16 GMT  
		Size: 52.4 MB (52445986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef97169c47ca52a8e66f6ef70d0a4d9e5cfae0f8b72d1937ac646b3bdf48d8a`  
		Last Modified: Thu, 22 Jul 2021 02:24:13 GMT  
		Size: 5.1 MB (5075544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e445910f582e1f6da040a3bdd8886f00fcc077bf63486317b6de7c17cf3ba01`  
		Last Modified: Thu, 22 Jul 2021 02:24:15 GMT  
		Size: 10.6 MB (10571845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d89631dabbc12408ce2f82d183513c97cde3d9b7ed0f3d4863be9777cbc50ed`  
		Last Modified: Thu, 22 Jul 2021 02:25:07 GMT  
		Size: 53.0 MB (52967486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395333ed39ca240b5db60aacfacb06c84d655f3442312ecf2b4b850dcb53e096`  
		Last Modified: Thu, 22 Jul 2021 02:27:05 GMT  
		Size: 174.6 MB (174647141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3bbba69fa1aa24a477bdf97e8d118be9d230ead53f6e3dd145b68c38bdfca8ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283065433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86550c2a375251e8b24ca5fefc6d52e668c5a2e84d7224c0849b9276d50c51ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:21:40 GMT
ADD file:10ae021b5b2998c7ee0904a6d9b6a3697ef580d3a6b0a0980c2f209a6ad2bb29 in / 
# Wed, 23 Jun 2021 00:21:42 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:49:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 05:50:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:52:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2bb9348ee5f2e424d70e44ac1d1e0b029bb37d72f6050453f93408edc2af9176`  
		Last Modified: Wed, 23 Jun 2021 00:33:47 GMT  
		Size: 50.1 MB (50105618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc10d3401b65a0651a08c5c29f2e1207dc4ca1027e80abc9b35cf15c88d96958`  
		Last Modified: Wed, 23 Jun 2021 06:21:43 GMT  
		Size: 4.9 MB (4936190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5dd2865193f1b761bf000f90190639fb8bfea0ce5033bf2de30ad2d9738789`  
		Last Modified: Wed, 23 Jun 2021 06:21:45 GMT  
		Size: 10.2 MB (10217331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f72f157f0331915f121358a516bb24081ca7d6310badb3e864d7a50a1e81882`  
		Last Modified: Wed, 23 Jun 2021 06:22:33 GMT  
		Size: 50.9 MB (50925879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de5a5d55da3a2a47047b4d592aed541e05a5e2b126f24f8000a484749c63b7a`  
		Last Modified: Wed, 23 Jun 2021 06:24:29 GMT  
		Size: 166.9 MB (166880415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:820012840a848628655b2dc92369233953308525356e5768abaf0325e583e33e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314369574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22bf6fb8a6691e3fea222fc871b3c0b5c1636a4bd1509c652d8f899865048df`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:46 GMT
ADD file:a3549e948b3f56a447f7f9b8c10f86c1915a2f52c546e1e7891735ee86a647ee in / 
# Thu, 22 Jul 2021 00:40:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:17:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:17:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62e8b52de22392fa7c459ae1bacaf43117fdae59adb2ad8b421412ace5a516b1`  
		Last Modified: Thu, 22 Jul 2021 00:47:01 GMT  
		Size: 53.6 MB (53593074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f26cc7a118272da0a6d22d8d2788a1a25d2f7e416cfda133a48219a5f1fced3`  
		Last Modified: Thu, 22 Jul 2021 01:26:21 GMT  
		Size: 5.2 MB (5159864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d208ca6539dbf6b41a01d767eb9b2904ee7a991935f60f061cd678987bc3b4d`  
		Last Modified: Thu, 22 Jul 2021 01:26:22 GMT  
		Size: 10.9 MB (10873259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8ab38b650bac84d69771a018e22df0bbc743711a43a0d444b551ac2aa10262`  
		Last Modified: Thu, 22 Jul 2021 01:26:46 GMT  
		Size: 55.4 MB (55406644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c70b2488051d7a2bc51c321edb04fda656355ea11adee20fa68587d2f2eece6`  
		Last Modified: Thu, 22 Jul 2021 01:27:27 GMT  
		Size: 189.3 MB (189336733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:181d47e67562d4c3f3b9ca903c35a03016f3f0c3efe212f1aea2d2e3359bd2cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328482384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a538e687e38e5b24dc8b7fd9930fdec147c20918b1f96d5f8bdb2b0ad792cf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:40:18 GMT
ADD file:20378fd7bc859874d8620bd807402968cbe571a1ca281d0f344392ed5d8af55b in / 
# Tue, 22 Jun 2021 23:40:18 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 00:11:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:12:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff9feaae647f307940e0b5cfdb30f3d3a877220cd3394859c1af4b3d653b2e97`  
		Last Modified: Tue, 22 Jun 2021 23:47:46 GMT  
		Size: 55.9 MB (55914853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5310b9c9dfb8fd34f5ff4cccb1d7af5e1baf20620d64357dc51a0e69717717e`  
		Last Modified: Wed, 23 Jun 2021 00:19:34 GMT  
		Size: 5.3 MB (5299879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab8c3b07912881a8d38f2ca51a04fef6fa1d22c0163da069cd226eec7362a07`  
		Last Modified: Wed, 23 Jun 2021 00:19:35 GMT  
		Size: 11.3 MB (11250598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66c7b3456d19d1557f96e2c7bf74716f3187c850af8e39dbbccf8890f4c354e`  
		Last Modified: Wed, 23 Jun 2021 00:20:00 GMT  
		Size: 56.7 MB (56666110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cab92909461cd5dd6672c529f1b219ba703293e42d3dd10ed7c87dc0273ca2`  
		Last Modified: Wed, 23 Jun 2021 00:20:54 GMT  
		Size: 199.4 MB (199350944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9968118e487f0cacd20e526db49283838f8071e7172d4d79508e684fb26d6cab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302161774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff19a9ebb326ef09057f763b14d1befbb9ef1a11fb1a319e503d234f3ce6fae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:10:12 GMT
ADD file:21823f99ac9631853baf61992ae48f9aaefd9aa14689bdad76945cbe790d4b23 in / 
# Thu, 22 Jul 2021 00:10:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:47:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 00:48:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7674bbd759fec6741d7d94cfebb5e0cf54c599cb2a824313eb96b1d6622a44b`  
		Last Modified: Thu, 22 Jul 2021 00:16:59 GMT  
		Size: 53.2 MB (53162150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbf92e62547174ba9022d0c0fe12fa84126289620f8148cf33269681b8273c`  
		Last Modified: Thu, 22 Jul 2021 00:57:29 GMT  
		Size: 5.1 MB (5130754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2614779dff3229eb62dc8a974d88a9bf60cfd085721871ad71d642e0517eb35`  
		Last Modified: Thu, 22 Jul 2021 00:57:31 GMT  
		Size: 10.9 MB (10873093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100254d07ca9795fcf9cb6c9e7d187591a97a9ac79c2b0c7c4351c8e7c1f30a8`  
		Last Modified: Thu, 22 Jul 2021 00:58:21 GMT  
		Size: 54.1 MB (54061422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6915e63e41945d00f1670a2473ea47b17b71197fc76299ad61b4a70568963680`  
		Last Modified: Thu, 22 Jul 2021 01:00:28 GMT  
		Size: 178.9 MB (178934355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c8c03893f4ef0f32ecf8097915982622171503c6738f04dfe46193c52e115f86
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337398197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115c1cfcf076dc5b9b920946ebafaa7cf9eddccd045e13ada9bce0fce4a0370b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jul 2021 15:58:42 GMT
ADD file:9d5a0ba0a24f9a37f3d9812637e4beef52ef27fa65d76c97dffa3f4933633701 in / 
# Fri, 09 Jul 2021 15:58:46 GMT
CMD ["bash"]
# Sat, 10 Jul 2021 06:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Jul 2021 06:41:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Jul 2021 06:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Jul 2021 06:59:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:28a36a9b0ca23da4474256976c303c139c5800da883d61fb1e52bc74123ba134`  
		Last Modified: Wed, 23 Jun 2021 00:37:34 GMT  
		Size: 58.8 MB (58812906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c65c32ac33fcec60fedd0b9e713bcf0f7b704d59b14cce6afa4a06e55e315a1`  
		Last Modified: Sat, 10 Jul 2021 07:07:55 GMT  
		Size: 5.4 MB (5421908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57141b1c3dd2e33c1dc87ff3220529d62b3a28a6e52333c04f525f64ebea0006`  
		Last Modified: Sat, 10 Jul 2021 07:07:56 GMT  
		Size: 11.6 MB (11626506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd24e3c55ddd1ed96c7c862a05ae38a752d0f3a6e31ccd516d38b1305735e85`  
		Last Modified: Sat, 10 Jul 2021 07:08:20 GMT  
		Size: 59.7 MB (59667524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50807d3f45f2c70b78120e0bf7f60ea2a799c8b6adac4543d279a5167b07211a`  
		Last Modified: Sat, 10 Jul 2021 07:09:10 GMT  
		Size: 201.9 MB (201869353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:74fd6fd43bfc9ac1b4ba6071a5bc55ac61cddaf64b7a8c70477997a172761298
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329223455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8172a85c0ae505fd55ce8d1624475ce24808e235872df6599e0dc6dc939f3d44`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:15:18 GMT
ADD file:b4e98baa24988a55379e3fdf724731b1139785071c1e2ca5d8e5adb43be85150 in / 
# Thu, 22 Jul 2021 00:15:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:18:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f89739902ab20ca21252189bdcfa682d2d8fa5c61d2bb714fe2fa6f3a5c519eb`  
		Last Modified: Thu, 22 Jul 2021 00:34:31 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc4d529e1e9e4423209e8cd25e27a2a6f2936444c4aefe731dff4f2182309a`  
		Last Modified: Thu, 22 Jul 2021 01:24:42 GMT  
		Size: 5.0 MB (4984778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31856dffc5e9c49615c1b03c06dd7711260172bc519c1d48536e27cbf15fadc3`  
		Last Modified: Thu, 22 Jul 2021 01:24:46 GMT  
		Size: 10.3 MB (10293785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a92ee8d3a71206345072e79dd2dbc21375b2232df7d85161732f650f4427f1f`  
		Last Modified: Thu, 22 Jul 2021 01:27:18 GMT  
		Size: 51.4 MB (51369171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608a5981d5ce91251275a746563b1fa4bb27029a7806fe0157a8d3e56ccf21e`  
		Last Modified: Thu, 22 Jul 2021 01:34:15 GMT  
		Size: 212.2 MB (212177993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b8819f0e38203dd8bf75fcd60cd974b628c9541c02219f53db68d600d0f8b843
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296247629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e432d06532cc6203507b6953fd578e1d1108a7591a81398919079f225b19ce4c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:43:01 GMT
ADD file:eb0fa0f991634817ac5af2d4e957d8d14c8fb5a8d501cfeb56949d715ca84f1c in / 
# Thu, 22 Jul 2021 00:43:08 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:18:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:21:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:730f0cea2dc4896e7a1a70e4e4e14165f66e42bcd880b7b7242a68c9d2ffa297`  
		Last Modified: Thu, 22 Jul 2021 00:48:31 GMT  
		Size: 53.2 MB (53187330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7d1fd11d3f6b43667d4ca70d209f8ae22c2e40a78c9c810ae7a0f944c04b98`  
		Last Modified: Thu, 22 Jul 2021 01:28:41 GMT  
		Size: 5.2 MB (5152875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a8f611511094fa5cccaf153c7a6dd4dde6a330473614087e039fa44ca58fe`  
		Last Modified: Thu, 22 Jul 2021 01:28:42 GMT  
		Size: 10.8 MB (10763675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420f67b72350ece22438f02a25c08026b757f5fc506536df3d9d0b2b294c37a1`  
		Last Modified: Thu, 22 Jul 2021 01:29:02 GMT  
		Size: 54.7 MB (54715565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c275436003c0a7abfe2b76caeb98cff5693b76a3a52a61b877732c50961ca`  
		Last Modified: Thu, 22 Jul 2021 01:29:30 GMT  
		Size: 172.4 MB (172428184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
