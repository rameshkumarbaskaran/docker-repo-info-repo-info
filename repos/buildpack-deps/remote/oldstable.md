## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:d29b531f43722076334061ae4e9d8e108e78e421b1c144556c46c58955dd558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:311968d39ea90ac3d005627daa6ad9b9f4206c1f39dd07e834491b99b39275e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.1 MB (325091606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13768bf8b4485233d22c6d2b71ad551936732bbd950d88043925c1ed1b05d33e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 05 Feb 2021 22:20:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:21:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae0ade158685a8e718a6afd2289fa52e5c5a38342a07ad5e1b3b2fdd1c46bd`  
		Last Modified: Fri, 05 Feb 2021 22:27:08 GMT  
		Size: 11.3 MB (11268539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911674ee9a5463a175abbfc4306db7b2debd5f54db613c089a57891c574b105e`  
		Last Modified: Fri, 05 Feb 2021 22:27:07 GMT  
		Size: 4.3 MB (4341873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6954b219f556b89ebe07d2807a9688f4caab3521c23858e82c487bb472bbcf6`  
		Last Modified: Fri, 05 Feb 2021 22:27:22 GMT  
		Size: 49.8 MB (49785887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801a158184b63e0482ad5347323de8b7ad05d5c658e201ad5522863696d5f63`  
		Last Modified: Fri, 05 Feb 2021 22:27:59 GMT  
		Size: 214.3 MB (214315293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fb097c3816a7a5b9648cb61e4d1a283133245b5f9a5e81757cc797e4adedc537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309053247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd657a6326047f0042cb645247c565b40196a38bdf3593b6f0a3524c64c4211c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:55:15 GMT
ADD file:3047f832191e46ed288c3efd5d017316fc7b7d8fbd282800d02da8ca0f799430 in / 
# Tue, 12 Jan 2021 00:55:16 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 05 Feb 2021 22:53:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:56:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99253078aee5285b1d9437ad45736eccc40de8b1007a23b3de45924452cfb0d`  
		Last Modified: Tue, 12 Jan 2021 01:04:44 GMT  
		Size: 44.1 MB (44091438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459df85eb788f77ccd902aad43fb54bc59c1fbc71afa1534ff2c07bdeba6cb4c`  
		Last Modified: Fri, 05 Feb 2021 22:56:59 GMT  
		Size: 10.3 MB (10319863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280716e09384aa70d6035e93415a3471fb57f9a1f918d5cfa8148cc48a1993e3`  
		Last Modified: Fri, 05 Feb 2021 22:56:57 GMT  
		Size: 4.2 MB (4161445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1ea0ee3a00775ac15c50fec332c0c01adc3551fdbaf4e115cc2db4232d16b8`  
		Last Modified: Fri, 05 Feb 2021 22:57:23 GMT  
		Size: 48.0 MB (47987741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94daff07ac6737556a4f695683056b7f28694398f90589835eeb77667d1ebbfb`  
		Last Modified: Fri, 05 Feb 2021 22:58:24 GMT  
		Size: 202.5 MB (202492760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c82d39063ff915f7ff9addece7f5b11b229b228ed92a57c0f01b16e788f22425
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297075133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698884b736edb5419c3820da2cf74f6299d77b0cf94eb4e4c19c86359eca457b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:05:19 GMT
ADD file:9c744a203d36aa8c515bbc11873a4a479cdf3fe9f020ca1ef207b53e6b3a251e in / 
# Tue, 12 Jan 2021 00:05:23 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:59:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 05 Feb 2021 22:59:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 23:03:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f5de2649c1cd9091872f81b8ceb6a67890124f113d9fce9c52bf60d5a6e19f43`  
		Last Modified: Tue, 12 Jan 2021 00:15:23 GMT  
		Size: 42.1 MB (42119951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f99bbdd939756c4a7dcb124462edc660d09e2897b4a63494756911fd90c7530`  
		Last Modified: Fri, 05 Feb 2021 23:09:05 GMT  
		Size: 9.9 MB (9913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1c64fd0b124f851aba2921933249306613c6e9294e28c79e41b8c960a6bcb7`  
		Last Modified: Fri, 05 Feb 2021 23:09:03 GMT  
		Size: 3.9 MB (3921097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb351752cf8e6d2968aabe250f59ad600c33f8cb4c05916d88a31c74b7a668e`  
		Last Modified: Fri, 05 Feb 2021 23:09:27 GMT  
		Size: 46.1 MB (46122154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af40a7bfd5634fa59b04f23b5216c6908ab98536ed92ba3cec8f6c91230028c`  
		Last Modified: Fri, 05 Feb 2021 23:10:26 GMT  
		Size: 195.0 MB (194998102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c30e0cd7e594301553b870807d50d6b3c85430dbbbb7ea0e80438ceb49e89d8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306894874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d079d8639d57c9046ea50ffc0f3ac4c0cd23e0dafd929a64baa447ca2016ad40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 05 Feb 2021 22:41:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:43:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25980bf93101cf6e28f2866b5d55dde2a817c6c5e5c9e82be93f55c872b9a9f`  
		Last Modified: Fri, 05 Feb 2021 22:48:57 GMT  
		Size: 10.2 MB (10182590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117548f2863b6d36f3c3df656a2e64c9847e7e6ee40e86ee1619be68045f47d9`  
		Last Modified: Fri, 05 Feb 2021 22:48:56 GMT  
		Size: 4.1 MB (4096578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987e230ca556e106ea8c9f27368246c668544e55254b5f874557c70d9a20070`  
		Last Modified: Fri, 05 Feb 2021 22:49:19 GMT  
		Size: 47.7 MB (47734077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca3ca727509ad83a28292466fde03f03fe581c31d20be44a42acfba1d5df89f`  
		Last Modified: Fri, 05 Feb 2021 22:50:16 GMT  
		Size: 201.7 MB (201703665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d3d6d97f8b13ec108dd80558c36a255274f0fdba96ee717886118eebf94bdcc3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c596249cebc84397ddfc27358938704a62f4e54f6d75c0c4526489d0e2f6afc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:00 GMT
ADD file:0da7fb4b520f7df6963291eabeab1e021ecc9f8fa5507ea307b64cd109898702 in / 
# Tue, 12 Jan 2021 00:42:00 GMT
CMD ["bash"]
# Fri, 05 Feb 2021 22:39:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:39:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 05 Feb 2021 22:39:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 05 Feb 2021 22:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9200bc3dda820226401b71a8464b0ea725d889387e461c9cf3d8155012f09f94`  
		Last Modified: Tue, 12 Jan 2021 00:50:31 GMT  
		Size: 46.1 MB (46097646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df48367c49a2330bc291a54c9a791fea1668482543526971a917d728cf2c9903`  
		Last Modified: Fri, 05 Feb 2021 22:45:58 GMT  
		Size: 11.3 MB (11318382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ba5108fa591e9842194486b8bf60b4f032b6baed2f73d3aad1039d08c0ff2`  
		Last Modified: Fri, 05 Feb 2021 22:45:57 GMT  
		Size: 4.6 MB (4564480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2da13268613eb419f2039d2f5bf72db698c2bdd2452438ab99694666a817500`  
		Last Modified: Fri, 05 Feb 2021 22:46:20 GMT  
		Size: 51.3 MB (51263153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e784d3b547e633895e0c5ed55f13fdc4ece115e8e6774a96bfa95bdef638e1c3`  
		Last Modified: Fri, 05 Feb 2021 22:47:31 GMT  
		Size: 219.4 MB (219370082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
