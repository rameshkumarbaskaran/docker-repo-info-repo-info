## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:d794d933d2e8bb76bbd9cc5cf0816c597efea9ad667782c4f6396be5b8be1ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ad38622b92c67227c9755ff9d713614dbb1a94d3d27bfe3431e74fb0810c2f65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406700291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184230a457ca527d91e3cf79b0e4f8605db36f1bbb8ac56c85b8d877aee988a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:40 GMT
ADD file:0255a38a25ff74df5705cfa360847fd81f98cc513707203d1e54a75263f54a76 in / 
# Thu, 03 Mar 2022 20:19:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:53:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:54:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:57:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec78bc49f256d7c26847ea612014b0bfd18cefe448e2b8e327512c6839fdba84`  
		Last Modified: Thu, 03 Mar 2022 20:21:02 GMT  
		Size: 30.4 MB (30385738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac486f3e51c4ec586a48b678184f79c60cc82e142eb10b4eefb4f894a0c8fa87`  
		Last Modified: Thu, 03 Mar 2022 21:06:32 GMT  
		Size: 3.7 MB (3694199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7dcc7b569cc2b1f8acc8b2ceeb11a411d6c50ffe47bfc0b5b2066864e7ed5d`  
		Last Modified: Thu, 03 Mar 2022 21:06:31 GMT  
		Size: 3.6 MB (3552116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf22a528a7f3cb392eed343fec636fc9ad1c71c0b2bc4597227679552be779a5`  
		Last Modified: Thu, 03 Mar 2022 21:06:49 GMT  
		Size: 38.1 MB (38085372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ca9f11e99ed3caa54ad3753a56737a90437cfc7f025b2811769cf1ba070e97`  
		Last Modified: Thu, 03 Mar 2022 21:07:50 GMT  
		Size: 331.0 MB (330982866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ecb825b4ba4182c2b50bb8b98bdc2df60232b22875c24a3a910eec7d6b3058b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371086262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d38ad60acd7ec85e386c1f32b14b024669929fd1e0c865ee5e7eb7bab339ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:26:01 GMT
ADD file:32cc6b42d18aae85f2e55c58db7c21d70958ea4042c5a3b3d02fa68db5507935 in / 
# Wed, 02 Feb 2022 02:26:02 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:15:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 04:17:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:22:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a304b5b67cb0f88e02dba858b3d63b14bf2910fe10c7ca354d66076202e5a43`  
		Last Modified: Wed, 02 Feb 2022 02:30:44 GMT  
		Size: 26.9 MB (26918632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9de4838f1f90e55ad9c88ab8510ca88acc10d1fda129ced40c0308ef868b78`  
		Last Modified: Wed, 02 Feb 2022 04:48:40 GMT  
		Size: 3.4 MB (3443309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19780ca1848b91057df1dfb6c124559c11d3ca6da5cd58de559a02530a6435ef`  
		Last Modified: Wed, 02 Feb 2022 04:48:39 GMT  
		Size: 3.7 MB (3742850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be245cc30c2ccce63f465f04bdf365bea00f0feb8003968073fc6ffa6ee6d040`  
		Last Modified: Wed, 02 Feb 2022 04:49:20 GMT  
		Size: 40.3 MB (40284568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b132e9dae92e41c2da17c573f14f645bf806caa482247760469b6925c47de2e5`  
		Last Modified: Wed, 02 Feb 2022 04:52:21 GMT  
		Size: 296.7 MB (296696903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8bc197a5da2152c2a78d1cb86feb1cfbfbedeaeb1787ae1286c2ad731ccc111a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399362498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f729819c49b43ab327170b838ae049227e8d3c13476b13c3d39af58c18eb4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:11 GMT
ADD file:0e8c3ab0e6e7f15d32d0e43c17409e1ad9e4c77cb87b27edcb23fd8bbd941784 in / 
# Thu, 03 Mar 2022 19:41:12 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:10:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:10:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:10:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:11:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:070b8fff765c544371e1499a46e470f8c2eeb6f493d1e9949af6b068f1208ad8`  
		Last Modified: Thu, 03 Mar 2022 19:42:58 GMT  
		Size: 29.0 MB (29031972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bb6800b180c2bbd9c0d917ea78669aa5e7110362527fc96692bdb2cd314ffa`  
		Last Modified: Thu, 03 Mar 2022 20:18:18 GMT  
		Size: 3.7 MB (3679015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd2a7b702ea3cee495ba3e01196c92f87bcd77f372d995d2ad1c555947e9da`  
		Last Modified: Thu, 03 Mar 2022 20:18:17 GMT  
		Size: 3.3 MB (3327773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4528b4c4ba1eea7093dab1e9cdb512996043c77118167e5e0cc564e63e7d18fe`  
		Last Modified: Thu, 03 Mar 2022 20:18:34 GMT  
		Size: 38.0 MB (38033546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79c48c53c3c42b32dcae316931674bcda55a10489feba01b420ab26a960be94`  
		Last Modified: Thu, 03 Mar 2022 20:19:29 GMT  
		Size: 325.3 MB (325290192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:74b3cc98cfb9ee1e2684f15602afb2eb17ad2e8c26fbbc1c3dfbc5c2a47d8f37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414322514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd447d66114f00a0129131d347411ccdf99adc885dfa81c31576699b18839268`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:54 GMT
ADD file:c9dbe94a6e712a5b1a894d57c1396be96b5bd702e90b77b82817ce85618dadcb in / 
# Thu, 03 Mar 2022 20:29:04 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:39:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:52:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0c4c4e967fa8621c96984594294f639a4d7ec13235867cbd56a506b4ef96bf1`  
		Last Modified: Thu, 03 Mar 2022 20:35:37 GMT  
		Size: 36.2 MB (36175818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8dd918329f318acaa93d44e882d2d310d61f08741b32bf697e381e348af61b`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.1 MB (4147822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f180d1cc1b110578ee29533ee2466d939fc44bb802f1c74ea0241c95d3e02`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.2 MB (4242315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb4c4d37a778e320b4ae12d134942515574fe1fd2706b3073ddaca573f7715b`  
		Last Modified: Thu, 03 Mar 2022 22:02:50 GMT  
		Size: 42.7 MB (42728193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9a48bfb4e4c07baf9a3a9b9619fb83b7ca66028760513100f3133990d9eb3`  
		Last Modified: Thu, 03 Mar 2022 22:03:57 GMT  
		Size: 327.0 MB (327028366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8ad0cdd52ec23e204069059c2be03757389abc9cd41f7488f6da3549d69d1603
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266373071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d697a7aca21e9f01b19a7f37a81579d7a3f0552ba4bdf47a2f564f77cb3fd3bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:17:50 GMT
ADD file:e036bf8d2d9837df0754ed0751c2cfd386039c558c517121d3a048a6a37b7afd in / 
# Thu, 03 Mar 2022 20:17:51 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:15:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9f00725c1dfb59f0dc5edf593a8b3a65a79cb2106fd1dfb0492c29b0d3d04a6a`  
		Last Modified: Thu, 03 Mar 2022 20:36:05 GMT  
		Size: 27.2 MB (27214379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149e59e6c41692bd9b82ac05ccf0b72418a256938af0b0286e7e720b6306ffd2`  
		Last Modified: Thu, 03 Mar 2022 21:53:23 GMT  
		Size: 3.5 MB (3490700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c849cddebc546bc99d5cc608c1a923dc6423d55265f9d59ec59e26220ccb015`  
		Last Modified: Thu, 03 Mar 2022 21:53:21 GMT  
		Size: 3.8 MB (3804196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f277852d32a879e685f74b12e655b389c213b4b96d4bf9f1c4abbbd8e193acf6`  
		Last Modified: Thu, 03 Mar 2022 21:55:31 GMT  
		Size: 40.8 MB (40767755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06796a85add0160c388b0906662fd12ddaed4e72d9c4f42a20230a947fb35063`  
		Last Modified: Thu, 03 Mar 2022 22:01:30 GMT  
		Size: 191.1 MB (191096041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a304c4698aa995c284986049af9aa0afa2daa10fa1e54abfddb3bedfc0c1f0f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367825754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11609ad1461b7b2d5fe426a83d5c9c7d5fe1fe5cac08f994b9370a8d91acd160`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:42:01 GMT
ADD file:e150af68d3db546783a6fafa964d1b9264cb1b35930b07255ce083fa0c40e532 in / 
# Thu, 03 Mar 2022 19:42:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:36:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:36:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:37:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e0cf59e92c5acec5ae595918f7a30d60c44156b11926f39465f58e2132619a47`  
		Last Modified: Thu, 03 Mar 2022 19:43:36 GMT  
		Size: 30.5 MB (30524528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7871093b66fa67764e2403a711a69a008b0941e41ea3b9edb6b89473ad18a0`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 3.8 MB (3763377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3fc096c211db0aeef7379615bb3126fc4a81163cc8fc1c0b54d1ada0869b3e`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 4.0 MB (3963395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e75021dcdcb9dcae8b7132547ff083a6cdfddda8976a3e188ac791c9884d2d`  
		Last Modified: Thu, 03 Mar 2022 20:44:06 GMT  
		Size: 38.3 MB (38327374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09409f7c801465e5b9b1a0b593d01585712f0af485a63bbb52d2fea25d333c3`  
		Last Modified: Thu, 03 Mar 2022 20:44:46 GMT  
		Size: 291.2 MB (291247080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
