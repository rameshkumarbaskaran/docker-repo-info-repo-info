## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:0c3878389805faa9d17cd799f4382780a9a81708cdbf945ef8a619f4dceb230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53c55d6ae5633e090c738317558db84afe5e71f1939d0cce407d5a6ebd3a4fec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312249282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b17fe82fbbe09bbc0907e370da10ccfdd78adeda152232d3f2a11879a0d2d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:02:23 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac34a4d7c330794ec24a76e7e58b50d4c8f6a2fc77ca958d83092c8962e7d6d7`  
		Last Modified: Wed, 22 Jul 2020 03:16:44 GMT  
		Size: 51.8 MB (51829832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0a7e6f20fbc38a7f19b3d07aa64262789970e984f390815f867ec783e4952d`  
		Last Modified: Wed, 22 Jul 2020 03:17:22 GMT  
		Size: 192.2 MB (192221104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:07eb390d00947811e3d97b6412858b7d60b0155cb9939967c46a1823618d7876
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285899441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893038cca12883cb2b75c5dd3632b131323c2389582ebb52bf08776d750d8058`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:50:16 GMT
ADD file:0431730a3850ee2a710a03ba04d05224938cf2f5318e1f73ed74677c70d09b78 in / 
# Wed, 22 Jul 2020 00:50:20 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:33:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:36:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71cf5632cfeb30dc5a7a7ccd4742a02af636cd970ef3a45bebc17d3f20b3662d`  
		Last Modified: Wed, 22 Jul 2020 00:58:30 GMT  
		Size: 48.1 MB (48107278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87dffc06540f2eca873274114a3d8d49684b38428e946f67b0b62aa848ae49c`  
		Last Modified: Wed, 22 Jul 2020 02:02:59 GMT  
		Size: 7.4 MB (7360981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad12a2dc68e08e793efc12362e49a16257506721c8074ee8361c242244763bc4`  
		Last Modified: Wed, 22 Jul 2020 02:03:00 GMT  
		Size: 9.7 MB (9686988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94df5576e4481b3422d3ba55ceb470a19b7245355de69b1ee3efb03aec34668b`  
		Last Modified: Wed, 22 Jul 2020 02:03:38 GMT  
		Size: 49.6 MB (49572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334d8faad6c3bf412589dea023c2eaf93157b9a20686a4154dedd09caf13a03a`  
		Last Modified: Wed, 22 Jul 2020 02:04:50 GMT  
		Size: 171.2 MB (171171824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5260a375a3b072b7233720c864214d890f577ea4b3887a51f0c691b52b961803
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278087223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa70698cd2d1e413e5b038d07eb0cef2d3caa43d5155f3f8513b0e9141afc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:00:40 GMT
ADD file:35073a186411c4b773a9d4d540ec0693ced845cb847b43d8465f9579174cd2b0 in / 
# Tue, 09 Jun 2020 01:00:45 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:46:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:46:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:48:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:52:12 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff0731da2e4f4a0ae8329840eb7fed7ea6aac11aecbfa15c6e684caec03920d`  
		Last Modified: Tue, 09 Jun 2020 01:09:57 GMT  
		Size: 45.9 MB (45868949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbeb0ded58d68be17265763fda36a4e1a520234a291d66f370d98a3e0d6e591`  
		Last Modified: Tue, 09 Jun 2020 02:11:21 GMT  
		Size: 7.1 MB (7097860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6159fbed770bb99a219eae06828da55caaa649879843c0b9df18ddda9b698b3`  
		Last Modified: Tue, 09 Jun 2020 02:11:20 GMT  
		Size: 9.3 MB (9343524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba732bafeb6b1467fd6908c64c6e8d10ffb27e44e3a25ab4c6c38e8f753baa5`  
		Last Modified: Tue, 09 Jun 2020 02:11:43 GMT  
		Size: 47.4 MB (47356467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d84f63917d0e3fb79c2b4c16f4595b8db444749589cfd28a57ef31188ab110`  
		Last Modified: Tue, 09 Jun 2020 02:12:32 GMT  
		Size: 168.4 MB (168420423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d6e3deda50a3f86bbdf7336348378fb4ab7a6e27c26e38f51c90ef5a974beb82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302746397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8958dc531db292c40a454b996739e514cf55f8a1d4f1084e9e48a4405b125a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:20:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6493ea016bd1aa68fa88d01d53cd305f67bae5fa500592c76c466808bf221`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 7.7 MB (7681419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33779eed82f6ae65801a87fd1278e902bbab0f609f0c6a0232d8ef0b37112127`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 10.0 MB (9983891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59beb1d7f774f0b2aa38b8043218a6d924bda1eef4f4692efeae226cded00a94`  
		Last Modified: Wed, 22 Jul 2020 01:35:52 GMT  
		Size: 52.2 MB (52156162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7211efa60e4409a04ec82c35f2f1536347fd0e0a85e23e3d952c51f329da5ec6`  
		Last Modified: Wed, 22 Jul 2020 01:36:48 GMT  
		Size: 183.8 MB (183756452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:394569056241ef5479837c7ffb7d66c85e655983f7ae25f64f4fa65f37a4789b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321669684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d005fd9650709a57c2fd272047d10efc283975c884f91d4487b76b3986b55db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:55 GMT
ADD file:2f4b8d9ab41b6e158f5926883b6bffdab1757086d903f3f0244f75bafc2e4876 in / 
# Wed, 22 Jul 2020 02:08:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:20:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:20:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:21:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88151d2519867746e4945a0a06b45430b9ddc2ae4be7e7f927cc00e3f640290d`  
		Last Modified: Wed, 22 Jul 2020 02:15:24 GMT  
		Size: 51.2 MB (51157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63faf17c1329ba4be1004b79b9d5981fdb34d19dafc018cddec9e666c9c34b01`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 8.0 MB (7981104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01afb186eafcffc2d1ca254ef5ee318f8bcb96ad9f552c6d73ecb3d5330e09fb`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 10.3 MB (10338463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33759e7774776f76867212a642bee66d5f4b1b73ce09b1af6b9504cbc769ee61`  
		Last Modified: Wed, 22 Jul 2020 03:40:35 GMT  
		Size: 53.4 MB (53429429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b645cbc6ec8759a3790b819961389d37eda083f5bd71c637d4e6f9de61104`  
		Last Modified: Wed, 22 Jul 2020 03:41:43 GMT  
		Size: 198.8 MB (198763491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f68fc2d5a367bf1b6b92d51852ee837a43e197a139d15f7522722daaebe213c2
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296855425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a290b8366d5540e9fede4f5b85c2fdbc47b2557d6f8753f9e9a103d31de232fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:09:44 GMT
ADD file:b51eae556569a7654c89a15b745fafdb0477ed08e8a06f7fcd6363145123d67f in / 
# Tue, 09 Jun 2020 01:09:45 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:51:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:52:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:55:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8084fc3b4d2453eb8005c0b33e3c542e3615868e22652e74e19fec36df3c488e`  
		Last Modified: Tue, 09 Jun 2020 01:17:30 GMT  
		Size: 49.0 MB (49019818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df088964944d43608e89126d7ae55a47489499bad77148bac16c1593e8ff69a`  
		Last Modified: Tue, 09 Jun 2020 02:10:24 GMT  
		Size: 7.2 MB (7231469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a34d1c06dc4557c94a0e8dc1d4f49ee8f512c443dea9748d2bb00fc4e1f6502`  
		Last Modified: Tue, 09 Jun 2020 02:10:24 GMT  
		Size: 10.0 MB (10015784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaedff7ebdd283f729f3eb0635079193636dc776885aa0339370ed36edfbc2f`  
		Last Modified: Tue, 09 Jun 2020 02:11:18 GMT  
		Size: 50.8 MB (50838846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814cc59ed9a88b832e8d53df38caa9b76578203bea7cbfc5b7c03b6d842221e1`  
		Last Modified: Tue, 09 Jun 2020 02:13:43 GMT  
		Size: 179.7 MB (179749508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:51ce445239fe23c5d42c7cf6c823e5930fb319da91991d220fd390fc3f788141
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.6 MB (333602054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01485470f351c0333085863f5fe144afa89030d0cc9f1f5d922a6cbd7fd66ebe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:01 GMT
ADD file:18a41180457a190a9dede1228479d2e332a348f22ac027c36e14d6d92e556f22 in / 
# Tue, 09 Jun 2020 01:22:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:58:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 03:00:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:11:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0cad52b1770a1b4a84068be3efe78098837be582f5905e627b2cdba07e641fd1`  
		Last Modified: Tue, 09 Jun 2020 01:30:12 GMT  
		Size: 54.1 MB (54143376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0318f8e4196d9f742fcca63ed04f9c2cb14ac6541f33cd67dae342ef35845da`  
		Last Modified: Tue, 09 Jun 2020 03:43:38 GMT  
		Size: 8.3 MB (8254819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec302fe954105553bdc7cac9100b6bfd114d3b56ef94d850b0364da83650fc6`  
		Last Modified: Tue, 09 Jun 2020 03:43:37 GMT  
		Size: 10.7 MB (10727191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf65a8c1ffe0371d22a42dfd9c0b4ac2900e0ca4d9d12502c488c59d3aff6aee`  
		Last Modified: Tue, 09 Jun 2020 03:44:31 GMT  
		Size: 57.5 MB (57460152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aad1912038650766f7c3949e5b7084d257bdb77914a13f32fc7334f57b1ee68`  
		Last Modified: Tue, 09 Jun 2020 03:46:28 GMT  
		Size: 203.0 MB (203016516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a6e859c43dc3636b69316faf69c57f6e1d363fa47312dfb4c4f3788ab9b2d3a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294376476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7476418faecaa658bdab3548bec9f5ecbc5d752c21a93280c74481582c65ffa0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:24 GMT
ADD file:e5fcdcbbd996899922beac57e202b7e0895321e07263147e96c6e3b7b811d8a2 in / 
# Wed, 22 Jul 2020 00:42:26 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:06:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:06:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:07:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:07:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ecdd8436fd4d951f4ca002a2aa8b01d427a7c4b535083e3ef0792444053154d`  
		Last Modified: Wed, 22 Jul 2020 00:45:30 GMT  
		Size: 49.0 MB (48966422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8e5cabcd07c3b92963e637fc22608613c8a9013bf41d621452d8827c71214`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 7.4 MB (7385174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a68e3c7fb279126bd2a86ecae67a5c1bd01806670cb45ad4367f30176fcdb7`  
		Last Modified: Wed, 22 Jul 2020 01:12:20 GMT  
		Size: 9.9 MB (9882077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0fa137f6994d756f1fea600570b23bd7bf9a0bd77a3fd5369f522e337d0e14`  
		Last Modified: Wed, 22 Jul 2020 01:12:33 GMT  
		Size: 51.4 MB (51369332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75e3ca80696c4afa40e6d027d3601c1794e5eaf350aa1c0d60352b0b2d2dbc3`  
		Last Modified: Wed, 22 Jul 2020 01:12:59 GMT  
		Size: 176.8 MB (176773471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
