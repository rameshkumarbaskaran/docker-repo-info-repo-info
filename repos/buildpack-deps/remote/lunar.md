## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:dddb6fff0d070cd13c8d3a500fc3b09463245f2a460e36f2735efef6c0adca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af2658ba3a6f7258b8f3080d7e05a5cdd2cad80602a2b4ca148464cfeab2ecd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263780096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d2f37697f3297b6956fb544f0996b369e90f05ffa6fa122b3680b793929ffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 20:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:08:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:11:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6c6b907db42b6f1b03645d7cd822afa676930182719410e133c9480fede45d4`  
		Last Modified: Wed, 03 May 2023 16:46:32 GMT  
		Size: 27.6 MB (27604112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db8f628eadae81eed04537247fbc6272b83d4dce338e7ca875143d8702c14c0`  
		Last Modified: Wed, 03 May 2023 20:17:07 GMT  
		Size: 9.8 MB (9781500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed7b5916395be6abd3a3f41069beb08289681b448f14afdd062a8d630050805`  
		Last Modified: Wed, 03 May 2023 20:17:24 GMT  
		Size: 44.3 MB (44342733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2840d3786a3c2687b5a39e7bfd15174aa15e16c2b5b14fe39ba86c87395c30b0`  
		Last Modified: Wed, 03 May 2023 20:17:55 GMT  
		Size: 182.1 MB (182051751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c7da625cf612fd219e0cca4dbf8261a20d642ad1c451f36f0272e4152ffbbfe2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228684705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ec6376a5f43b6f581628fe97466b43ee950f443e00d8376277fcdd5a2c9ca5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:07:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8f976bcf9a33d090294b25c3fb3430a5833ce92be9f477471addb457c0dc3ac`  
		Last Modified: Wed, 03 May 2023 22:12:58 GMT  
		Size: 25.4 MB (25437887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653ea3e4c9dbd15b264a4a6a10dddb593e3d21e899c82f1684533e0b63e3191`  
		Last Modified: Wed, 03 May 2023 22:12:56 GMT  
		Size: 9.1 MB (9103832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51bd461eaec416e884ed0c9598fa7c90d7dc6a5ce5f4cc445fcd549b5b56c38`  
		Last Modified: Wed, 03 May 2023 22:13:14 GMT  
		Size: 48.7 MB (48687458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d0c7a1753d3482a2d9de3ac15c1eee33240085fe9af26d76f3ad235262092`  
		Last Modified: Wed, 03 May 2023 22:13:42 GMT  
		Size: 145.5 MB (145455528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:065a889bc9e068419d85da5818b142e54245c5aaa42b564d9fa95f12f4afe6c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257886516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cb60b5d6b0bc39f28e36ad7569d4b3f03bf447659023283338d36b04ea6d53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:53:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eedec38ef10e1ff872f423ceae12828c5413c8183c216098c34342de77e9e5a3`  
		Last Modified: Wed, 03 May 2023 17:40:37 GMT  
		Size: 27.0 MB (27017867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b19b0b741f1c54f6a360843f1321028128af5d283a1d8f0f5f66bf8beece0a`  
		Last Modified: Tue, 16 May 2023 23:58:57 GMT  
		Size: 13.3 MB (13349536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ede9cbd1d38078a543a2cb21cdb02b9aad695324d7f312340903eed543424da`  
		Last Modified: Tue, 16 May 2023 23:59:11 GMT  
		Size: 44.2 MB (44193854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05007a531a0678750be4d03a8d06029a4009ab0e91e443bec7f3d95d76dd788c`  
		Last Modified: Tue, 16 May 2023 23:59:36 GMT  
		Size: 173.3 MB (173325259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:762fb7cd6ddc02524c21a00a8518b218fa1f9719f3b433f30632b76ffd62c5cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288310662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260ac439e8e0ee6f0d61b6a9c6a9950fcc3027caa9439be38df0618382a7b59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 23:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:29:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:34:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff954998e64505d58ea7cf2bf1a248c9fdc2287c6f6c0f41d3268aa8df574bb`  
		Last Modified: Wed, 03 May 2023 23:42:18 GMT  
		Size: 32.0 MB (31996798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e392eac2e54d3ce287c6ad52608235e58697dd34630b471eb3e306bf35c2a09e`  
		Last Modified: Wed, 03 May 2023 23:42:09 GMT  
		Size: 11.5 MB (11489279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d337a20f31a2c377c8923ba928c77b4a5ad0c78cf2c281f4ca0e3a1a98b29`  
		Last Modified: Wed, 03 May 2023 23:42:43 GMT  
		Size: 49.0 MB (49040899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f611a05bcbe8fe35cd1d69f90fe2664bcb42e72fd7219c024afaaf2e241c2a5`  
		Last Modified: Wed, 03 May 2023 23:43:40 GMT  
		Size: 195.8 MB (195783686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f29d902b25a9e5ac1df71447b0d740098e154e0c7de74335c6b52574af421e47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239853727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2e4f1c92e2a6ac17001c937f1f55a4437d6de03644c97c3edaa47f431fd987`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e12ee780e94e13677b8efd3cfc5219f323ee331fab05eb1f1c59218a106122b`  
		Last Modified: Wed, 03 May 2023 22:34:25 GMT  
		Size: 26.2 MB (26236160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc738121c9813521fa4a0fca88e02cb1f66ef200380dff38dd077ab483e2c4b`  
		Last Modified: Tue, 16 May 2023 23:57:26 GMT  
		Size: 14.0 MB (14017600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b0c0328488d708fd92c4400fc82d0ff82947be475b2cec1e956ce34dcb9057`  
		Last Modified: Tue, 16 May 2023 23:57:37 GMT  
		Size: 44.2 MB (44222835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3867deac24c206cbbdaaf96a8901dba7a491dab5a53d2a5db0793912657844`  
		Last Modified: Tue, 16 May 2023 23:58:02 GMT  
		Size: 155.4 MB (155377132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
