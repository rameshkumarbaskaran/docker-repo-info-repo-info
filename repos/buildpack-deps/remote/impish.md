## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:5d3e4389621b55daec976494d8544cbeb9c2e53d6db67674fecd1429104ff79f
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
$ docker pull buildpack-deps@sha256:74e04bcb4ce77c2f7f498ceedef4bcd22dd482d3bd751c9860c2ae0b5940eaac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406701540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f2dc8d354435cd0cd1ca02df54d39a82b73e7316f0378acb7c272ffa7ff7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:49:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:50:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:55:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee29a8440a917a1f49c8a66657a5f8a8c2effd9e25b3bb9367ee85276d079b4`  
		Last Modified: Fri, 18 Mar 2022 07:11:01 GMT  
		Size: 3.7 MB (3694257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30247b645fd7fa468adece5509844320b82b4af192c0633c03785f1304e95c7e`  
		Last Modified: Fri, 18 Mar 2022 07:11:01 GMT  
		Size: 3.6 MB (3552145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b435325fdd0055e7dbb9c2e27ca4c08b8206afc1663c4c8d7cbedd1830a4f6b`  
		Last Modified: Fri, 18 Mar 2022 07:11:20 GMT  
		Size: 38.1 MB (38085451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa059c5ef6b1dd2e695c85aef87bbaa2149230373de2bb7f0c6741cd00489d0`  
		Last Modified: Fri, 18 Mar 2022 07:12:29 GMT  
		Size: 331.0 MB (330983777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a75937fb3add510c6703b0505eed435280fb553891531a4aa375d87136433fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371090239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe6a76f529619d8d949f4e424a76f1ff2336ca7ab7f55fe1d55765a67b49762`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 07:33:05 GMT
ADD file:380138b8388e9dab10885559d020801299e8a053731bc61eeac23044d83317c6 in / 
# Fri, 18 Mar 2022 07:33:06 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:14:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:15:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbf944519806fa77357b54f48091ca8c7ccaea62ebbb79761a15cc513dbcb20f`  
		Last Modified: Fri, 18 Mar 2022 07:36:56 GMT  
		Size: 26.9 MB (26921466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10b93b08ad29a35f3e5c193f2bfe6b9f9e7d502ebd11b72f4aa644268f77f99`  
		Last Modified: Sat, 19 Mar 2022 03:45:36 GMT  
		Size: 3.4 MB (3443108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e15c098c0600535f00359aaa245c8a9bbe723d52157f0a5df1dbe5fcba6d6b`  
		Last Modified: Sat, 19 Mar 2022 03:45:35 GMT  
		Size: 3.7 MB (3742619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887aea08d6ae55f9a1408735ea11709c157a49cafae9637ea0f94abb79b667ab`  
		Last Modified: Sat, 19 Mar 2022 03:46:16 GMT  
		Size: 40.3 MB (40286145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5089eebc8f352e98caa04d67863156d0c76cf4d120c89db1deff3895ca1b3`  
		Last Modified: Sat, 19 Mar 2022 03:49:18 GMT  
		Size: 296.7 MB (296696901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3813ed97afb025d535f346d4ab28f254b00387317880e3e58453ae1b877f7a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399362631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a356c02fe5a2ff75743ba8b5c8956a25f631179da38dd7da0c42fe4a7ed4bd2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:41:01 GMT
ADD file:56e2a8525a84b94f6a53c0931b691b54172d93bbce2289a0436993c0e3d0fb18 in / 
# Fri, 18 Mar 2022 00:41:02 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:17:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 15:18:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:19:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6dc4e90ace614f005604aea3938bb52d80702a668803ce72e3f02a04afb1e618`  
		Last Modified: Fri, 18 Mar 2022 00:42:56 GMT  
		Size: 29.0 MB (29031071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33161320fa639032d79afc222634260c4931da40beceff433eccac97b980ddb`  
		Last Modified: Sat, 19 Mar 2022 15:25:25 GMT  
		Size: 3.7 MB (3678508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c663ad73a7ede204c5f58ccc979c5a215be522eb0443423944274c4aec941`  
		Last Modified: Sat, 19 Mar 2022 15:25:26 GMT  
		Size: 3.3 MB (3327223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a729ae6292075a61a2f3ab04dc7f19fee7051d87baf58756ea3724869527ff4`  
		Last Modified: Sat, 19 Mar 2022 15:25:43 GMT  
		Size: 38.0 MB (38033019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2047eeff26627a5e44b0d4078d455add7af0917dc90c2c0e01e27138339540bf`  
		Last Modified: Sat, 19 Mar 2022 15:26:38 GMT  
		Size: 325.3 MB (325292810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e46dc2e0ca0a7ca3d8fac05367c0068a38e94cd7095cd4880c6d3cfa572df40d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414306529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0f4e5ecf96a15f9c389a41a3a2ef766171515219b0c4d31e3d70503442386a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:52 GMT
ADD file:89858932cfb6a302dee1bb3c3241eca7e3237f57c94d96b1d26c1501eb773148 in / 
# Fri, 18 Mar 2022 00:49:03 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:26:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:27:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 06:28:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:33:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38e6e8940c9b0e7d57e3a21acc8bd9195e70bafca6ac4cdbfeb38c31e707596e`  
		Last Modified: Fri, 18 Mar 2022 00:51:45 GMT  
		Size: 36.2 MB (36176038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5874cd22357e379148563268dd1cc6a4490ec2893788def00b94e9b392c90cd4`  
		Last Modified: Sat, 19 Mar 2022 06:54:55 GMT  
		Size: 4.1 MB (4147848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493554808f41665a8830cd429e29999e139641d2449c739e76563e6f63cf420`  
		Last Modified: Sat, 19 Mar 2022 06:54:53 GMT  
		Size: 4.2 MB (4242210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27338d8fa47aac4562e47c84e5ce3fd9ceb722739dad2bd9208715c56e778e8d`  
		Last Modified: Sat, 19 Mar 2022 06:55:49 GMT  
		Size: 42.7 MB (42723303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221cbd76c804955bb8cb1d612b0e64d7de25aa66597478182764bbb3ed0b936`  
		Last Modified: Sat, 19 Mar 2022 06:58:36 GMT  
		Size: 327.0 MB (327017130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:deffede3e6fdec826b872957b218bab93b2fe96730805df900f4a0decb8660fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266377994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc3d20896023a17f6c2ecffec4ba41be76d71f39f48441553e260a77d39b8a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:33 GMT
ADD file:52433e15e49d335dfc7bbc78550a32b9e0fa14eb31fae0ee2600087827048035 in / 
# Fri, 18 Mar 2022 00:40:34 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 02:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 02:58:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 03:02:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:08:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d4dcb4c786a507e8054e237dcda4d54fecb228f526b4716da0b3748e4e9c9d`  
		Last Modified: Fri, 18 Mar 2022 00:58:59 GMT  
		Size: 27.2 MB (27214441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d018cc194635cf808f308a016bf556df0c929bbaeca2419ddd072f327e7eef22`  
		Last Modified: Fri, 18 Mar 2022 03:39:27 GMT  
		Size: 3.5 MB (3490494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316dd6f0f2b9e02907cd326ff95e0950fc92c02a622066c5d1f6cfe1cba12da`  
		Last Modified: Fri, 18 Mar 2022 03:39:25 GMT  
		Size: 3.8 MB (3803952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902635f9f6391d0ff49d9a5ec92a582053c43b14a45c73d99c5d11695f8a1a4a`  
		Last Modified: Fri, 18 Mar 2022 03:41:37 GMT  
		Size: 40.8 MB (40769200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb6e159f66cc0955e900209ae54fabc0879193f42e007caa197592a19e487ed`  
		Last Modified: Fri, 18 Mar 2022 03:47:40 GMT  
		Size: 191.1 MB (191099907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a7f8d267e9582792cf29b10e5643f38b5f917ed451f34202280f28d41baba6ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367825425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc555c40caf455230cd29eb21cad611dc8ca46617d46413cb5b36cb03328eb84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:25 GMT
ADD file:d60e8b8e69d4d7cd336322d2e06a347240bee5422aa987adca502f206bf302ad in / 
# Fri, 18 Mar 2022 00:37:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:09:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 17:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:10:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:87cfc1a8b212d0c93ffba2243f10c74a3b48bab99abb783817e2837da77b60e4`  
		Last Modified: Fri, 18 Mar 2022 00:38:58 GMT  
		Size: 30.5 MB (30524462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec473927e23e8a21c53e75da1b7aa85c01c4d3691b465d156724173846cafa9`  
		Last Modified: Fri, 18 Mar 2022 17:16:04 GMT  
		Size: 3.8 MB (3763319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538edd1ce2ff65ce1cb1d47bf7d83c52f047a7e8eb952fecb42538ac156add8`  
		Last Modified: Fri, 18 Mar 2022 17:16:04 GMT  
		Size: 4.0 MB (3963400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9c2fb26e79155febfcaca74f1561aac203d22cf073823dd8433ca440aca5c`  
		Last Modified: Fri, 18 Mar 2022 17:16:19 GMT  
		Size: 38.3 MB (38327999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd25761c4ecc3464c0dcaa19e7b910c123edcc58061609455bea9565e8801c9`  
		Last Modified: Fri, 18 Mar 2022 17:16:59 GMT  
		Size: 291.2 MB (291246245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
