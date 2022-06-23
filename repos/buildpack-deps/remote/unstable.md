## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:66ec7a88af34287f09d34e0ec3aac9fd4cb83191aa53a8a32a193e7b0341b6c7
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
$ docker pull buildpack-deps@sha256:a248c9e612f302d4a30e3542d9fabc7ce0eaa41fa030e77c93282885a47dd813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341213527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3ee4df0d6614cf40d03c049831dd6fbd41a304a37142158c51c4b69d19479b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:33 GMT
ADD file:5d253befef9729db59927d6e0d60fc3d68d46edea7e014babd24f72ac3a437bf in / 
# Thu, 23 Jun 2022 00:21:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:53:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:53:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:53:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:54:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3673f28ea1768e72855620961143c989d7f371e6bca9954aea151e92c37b180`  
		Last Modified: Thu, 23 Jun 2022 00:28:29 GMT  
		Size: 53.2 MB (53218973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ae65eee62be843f104a65e140f50abf4d3ec55a20e85b9e3f7d2cfad04120d`  
		Last Modified: Thu, 23 Jun 2022 01:00:54 GMT  
		Size: 9.3 MB (9292311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6091239aaf7cc50884c05faa6c40bbdf0de0a133524daaebd95e5128d36a0d9`  
		Last Modified: Thu, 23 Jun 2022 01:00:54 GMT  
		Size: 11.3 MB (11264406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0035db86f2c4cb2e7be73d8634723047f8cca5c7260b8e2792b5d7a795402`  
		Last Modified: Thu, 23 Jun 2022 01:01:13 GMT  
		Size: 58.0 MB (58008546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8db46c1b634869a302a9753d2f062948b1cc5fa97e00f48d55b70319fe403a7`  
		Last Modified: Thu, 23 Jun 2022 01:01:49 GMT  
		Size: 209.4 MB (209429291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:27444e860eab9366fa0e3c89857cbad92d526cbad91fcf0e93121f1740b6ca1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309590239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d132ff5fce9001e82fc52f8ad28fecbba8181711b1958330b34de1661e55e2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:06:33 GMT
ADD file:e64ba6aa11d10902c0a4ef8d3e05a21ff17f500ec2beb0d0704f12a033eecd07 in / 
# Sat, 28 May 2022 02:06:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:15:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:19:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84223462af5a86d80ca0b6ee4295740a256dc6c036fd9bf8911e3d45aac34d9e`  
		Last Modified: Sat, 28 May 2022 02:23:20 GMT  
		Size: 51.0 MB (50961426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f88c92295b4fa5d01d5c7dd27b573f1426efbbe47348df31dc55de977a42f8e`  
		Last Modified: Sat, 28 May 2022 03:36:29 GMT  
		Size: 8.7 MB (8725167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb95b40f6f03c3c9f4041396fccdad464a167dcdabf7faa4ce59545b10eff9e`  
		Last Modified: Sat, 28 May 2022 03:36:30 GMT  
		Size: 10.9 MB (10927897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af801cca276fe8a8c2fa1f3f2f395ef1bf390a44b25cbcd5f6c27c81ee430fe5`  
		Last Modified: Sat, 28 May 2022 03:37:20 GMT  
		Size: 55.6 MB (55639049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658afdf25f2e6775d484a7e45081dc44520de0cccec63acb63e5cdc458e0b549`  
		Last Modified: Sat, 28 May 2022 03:39:23 GMT  
		Size: 183.3 MB (183336700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4b49b903f4a605bf006634512ba3446fdb753f01d7967577b13e41d6ca9f0987
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296398553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55be5dd021b0dbc7138f8b48b4f995747e08635f4f1d80458f2f85578e66c83a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:03:25 GMT
ADD file:8021dbeb20862f976e9f6edfab38dfb8756a92dd1ede73d49af4c657334e675d in / 
# Sat, 28 May 2022 01:03:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:50:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:51:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:53:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0e42766a606a457d26f0182502f6f1920959f31aa96f3bea8438d9c1662a0e5`  
		Last Modified: Sat, 28 May 2022 01:19:59 GMT  
		Size: 48.7 MB (48693491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c18451f312662604904a27a75c2a619f95996c3f8953c2894835994ef1938f`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 8.4 MB (8394033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ababb74aefd4519ecdc1de94bab8271fdc2ba7a6a0b2288e65d7452f33cf91a`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 10.6 MB (10572851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a64aad191116b0a523175f0713d0852be12924ca13142989d6feaecc7dd86`  
		Last Modified: Sat, 28 May 2022 03:15:34 GMT  
		Size: 53.6 MB (53563481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b718326b52a435522150cdb4a4eb7ac5e54bfa12a581db5599491436e16dfab`  
		Last Modified: Sat, 28 May 2022 03:17:23 GMT  
		Size: 175.2 MB (175174697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:73912f4ea4e298c27d013c431e0e82d2b3c8c53cdf6f13253ac5da6e877c05b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333799216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb998f99f9ebf55865396e5f52db4bbf22a8b66dc8c767c0f51f52030105ae1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:04 GMT
ADD file:f08e8dd302c69f11b0631751a00fb9468d4bd358c6e3c34e364eae4601f0a325 in / 
# Thu, 23 Jun 2022 00:42:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:14:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:14:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:14:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:15:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40490949eb8203de1427980faef5b6b648ec81967b0cb93ef80fb4a09d798555`  
		Last Modified: Thu, 23 Jun 2022 00:50:02 GMT  
		Size: 52.3 MB (52287486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd1881ca7c4691be4824f0eddf333c4f2ab5f1ac743ee1c8c554a75da079933`  
		Last Modified: Thu, 23 Jun 2022 01:24:16 GMT  
		Size: 9.1 MB (9132621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852bea5bd7a74a6867d8c61780e5bdaaad07e160db0bada549bc1b04e63e489`  
		Last Modified: Thu, 23 Jun 2022 01:24:16 GMT  
		Size: 11.0 MB (11041937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bb12213e9f6fc3859b16595e8478ff8f3156869e99a0f9352d29da9911e50e`  
		Last Modified: Thu, 23 Jun 2022 01:24:36 GMT  
		Size: 58.0 MB (57991660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7edf2182edbb15cbfc18bf1ad2ea2ba5e844c82e2cce4d13a8428d2dd43670`  
		Last Modified: Thu, 23 Jun 2022 01:25:14 GMT  
		Size: 203.3 MB (203345512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de27c72c84f62bf5ccf59944bb175468b69b7759871c4030d7a9c6ed9c370b9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.3 MB (344340026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66427b10aecf14660fc99e017f4dd75bb5369f7afd48f4c95dfb64f8aeaa5fa4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:59 GMT
ADD file:8e587a340c6b6c6dfa097954552e77cf8a794c99a1462d0c2062dd4f3b905687 in / 
# Thu, 23 Jun 2022 00:41:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:15:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:15:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:16:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:82252cde47e9fb82645e6353c13b39594115b4ab4b96e5a602245359036bb69f`  
		Last Modified: Thu, 23 Jun 2022 00:49:29 GMT  
		Size: 54.2 MB (54181034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a804107ac0ac6b959662ec593acb07f7f7900f2753d01cc321b3f498797ff54`  
		Last Modified: Thu, 23 Jun 2022 01:24:44 GMT  
		Size: 9.5 MB (9465816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3278139543c9edfb79cec19d272bb6af19642454308507ba2015c252c4b5462`  
		Last Modified: Thu, 23 Jun 2022 01:24:43 GMT  
		Size: 11.5 MB (11464249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553753d1d94d5a84b19b44ef5dd89152d8c95834466d6f78894d6f8d41a1c878`  
		Last Modified: Thu, 23 Jun 2022 01:25:05 GMT  
		Size: 59.5 MB (59495261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0627a1c61c9ae9be7e61d922c5f79dc898ae8348e68a35f1b27b148e492375`  
		Last Modified: Thu, 23 Jun 2022 01:25:40 GMT  
		Size: 209.7 MB (209733666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90b5ed050acbddf9a8c694e0cfb40890a2e7394294545223d626c4ed54061c8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319197229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7f494a1755d791268f8ebcd383e081d1cd611287b247bff036e5fd840429a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:06 GMT
ADD file:1687a4039bc00edb9de7ba18be7ce08c7df3d2cf6a4b7a30cb5bb60f41d3c082 in / 
# Sat, 28 May 2022 01:14:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:12:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:13:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:14:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7336e150b70b2115ef0d770279f4e6f79de8d6e16c87dd256445530c1c68d1e`  
		Last Modified: Sat, 28 May 2022 01:24:53 GMT  
		Size: 52.3 MB (52283200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31486dae68c1e92361c28f610c582d55f682b8dc91e6fadc6ce7d2f167d0f8`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 8.7 MB (8654895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a846f26a733756e5b7a30ab3e72a8147961effdf03d7e9b981808ea3ffc7a6d`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 11.0 MB (11019421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f22fde9ffb3511f19f6a84ee5511872740b6a37e844fdb93326adc895f8dde4`  
		Last Modified: Sat, 28 May 2022 02:31:27 GMT  
		Size: 56.6 MB (56621054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835cb71964c0b8f5e94466a46b6d004b0f3c861bcc1c853a3f3e279f27a4ad75`  
		Last Modified: Sat, 28 May 2022 02:33:37 GMT  
		Size: 190.6 MB (190618659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb498fbfff93344ba755ba5b6c26910bf43459a5eab2ddac155602fd7c9c8063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349476888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f165ccb43b3dd0eed4e187e01a69a05c356c16d5496633954ed24d03e48dc3d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:25:12 GMT
ADD file:ae9857e5f5e911c083920a02f175061f1626b33e8244c6b286b16a61fb6326ab in / 
# Sat, 28 May 2022 01:25:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:23:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:24:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:25:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37e804d95f71e07756995895c16c589fb7c512c0b5fda75c9e57d4ba10ea4c27`  
		Last Modified: Sat, 28 May 2022 01:34:49 GMT  
		Size: 57.4 MB (57378472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7461effc372e5ee4bd7909ed036e44f7b839da66ba136f7add0d1221c18cbd`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 9.9 MB (9880924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a54c3d4f16e2101943055448a74b563c54f32ad957a68eb5dba4c980373c3`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 12.1 MB (12065230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d030f83cb04ad5b06d1396bcda4925db17a6880b92c2161c73a4a52615c076f`  
		Last Modified: Sat, 28 May 2022 03:38:52 GMT  
		Size: 62.8 MB (62755153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5805742b88e53045692feebd6eb6ebb29a36560266cc5a98a48b0521259d2c6`  
		Last Modified: Sat, 28 May 2022 03:39:39 GMT  
		Size: 207.4 MB (207397109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:eaced6d7e07d3740cb04bf1d67f251c3ec5d90afadd06bbb4ea6f52710b6c6f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 MB (357755251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95454dfa3bf1b091ba4462e214d0e316b8195c46a0b0cfc1ed34a83ccc2a501a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:59 GMT
ADD file:e8683ebd7fe3c7f8d36edee19a4eb44173d2c0533a248bb49edfe18fbbec52c4 in / 
# Sat, 28 May 2022 01:15:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:03:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Jun 2022 07:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Jun 2022 07:31:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fcc51d6aaca235d0204fa542679e8c928a4f929dacf2d472c004f8bef16292b`  
		Last Modified: Sat, 28 May 2022 01:33:36 GMT  
		Size: 49.4 MB (49398978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11875dbcf4bf154b85cc0b226364129a3a766fd9696699dece93ac84fc30ecff`  
		Last Modified: Sat, 28 May 2022 02:44:06 GMT  
		Size: 8.4 MB (8388372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcaa3fee1a4ad6e285aa0e16f72b33694c419b2821bdeec5341875dc49f47c6`  
		Last Modified: Sat, 28 May 2022 02:44:07 GMT  
		Size: 10.7 MB (10650485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e27ca9c7481f28619ddde6f60a59911202108797689731eb9c1350eec0ebba`  
		Last Modified: Tue, 21 Jun 2022 08:11:45 GMT  
		Size: 53.9 MB (53944496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38281b0767ed61c43891ec0335ff72f28e950bc70cee9d2d8b939fe4761718de`  
		Last Modified: Tue, 21 Jun 2022 08:19:12 GMT  
		Size: 235.4 MB (235372920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8a628a52c7b4514d1ebb244681064d85246ba713a0dea58c4511639c40675d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.1 MB (311132458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3723b6ade3186d99c292614f3652d55aea2514d024e92fbe047f46332a7c45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:45:16 GMT
ADD file:ab375e0cb8f5b6409d63f919593d858353b72a1583cd317ab360dfe14ea03d6f in / 
# Thu, 23 Jun 2022 00:45:24 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:25:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:25:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:26:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:28:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8cf7e6e484c650a0d73e79e1cb371750be4da7ee1f80e6f2269ce876a0da394`  
		Last Modified: Thu, 23 Jun 2022 00:53:20 GMT  
		Size: 51.8 MB (51752635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f7c9785fe37d8cf623f10d952220284ffb99daa61aee3f8346d128877bcd24`  
		Last Modified: Thu, 23 Jun 2022 01:36:54 GMT  
		Size: 8.9 MB (8939375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282f27bfdfd818dfca8564ec63da5207a70fc4c2e78f1f0c5fe96ff585343b31`  
		Last Modified: Thu, 23 Jun 2022 01:36:53 GMT  
		Size: 11.2 MB (11157558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62041429a13a43bfbfd7d47a92db7f8c23e3aa09f835ed06612710629f88b9a`  
		Last Modified: Thu, 23 Jun 2022 01:37:10 GMT  
		Size: 57.3 MB (57299234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f58e17f4530843d986c8dc0f94c4cf87db72aee666923fbcb9f0eff4695be1`  
		Last Modified: Thu, 23 Jun 2022 01:37:38 GMT  
		Size: 182.0 MB (181983656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
