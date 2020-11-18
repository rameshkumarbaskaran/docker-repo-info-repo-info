## `buildpack-deps:jessie`

```console
$ docker pull buildpack-deps@sha256:fc37e2d7414abce6a4066b5b90304285b76c54a46db68a924b6c3c9d96b42d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:57f811160890ce7c0c46d6bbe92f213eef5d8ee6034298ef97c395679917b7cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247183660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa202761897af59d0cafa1553ea926d345d33402e247f7da6ed022422311a1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:33 GMT
ADD file:7b9ac38d270ca27e5fb553f80effa79883356f259ca9c3a1386f94c504626233 in / 
# Tue, 13 Oct 2020 01:39:33 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:18:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:20:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:22:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c57dff6aebdc848ab6cb6f56e094fe0a36bfe02230a16dc07e3acc5afc7f455`  
		Last Modified: Tue, 13 Oct 2020 01:48:35 GMT  
		Size: 54.4 MB (54388880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46109a4143b58cf9597de61dcb265516944d45ed3effc5ac56e1b90603402dfd`  
		Last Modified: Tue, 13 Oct 2020 02:29:40 GMT  
		Size: 17.5 MB (17545958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de80346457dd30540ff7023878d7763dc29bf4d350ce6dbdefcc40978f9984c`  
		Last Modified: Tue, 13 Oct 2020 02:29:54 GMT  
		Size: 43.3 MB (43335106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dbf70b523a23bb3f9b789f845c9ad58c6d7c25ad874ecb3dc19042f6b4a734`  
		Last Modified: Tue, 13 Oct 2020 02:30:20 GMT  
		Size: 131.9 MB (131913716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:58d94fafd36d36c4b07e7bbe7f578c1553394d82ce15e88bf2158d8a5477cf24
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227156326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9c23617c0f9df850555113995047eb78f26c31409a76ae9a3324f4035cfa56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:09 GMT
ADD file:06d0d96a3590043e004bbd651614b8c1b4b048df6ce8706542c12613e2ef83f3 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:47:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:48:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2950e78c0ac6ca79b0455caabb98b5d25fa715881ced046fe07f25029b96bd01`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 52.6 MB (52582709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d215fc87b1798e34927476d1004914e87fa45af53379310422e62443ed2654`  
		Last Modified: Tue, 17 Nov 2020 22:10:02 GMT  
		Size: 17.0 MB (17037302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af54c82019f8f5925604f7d31a5b391f3abbddce89539670db949eb979855c82`  
		Last Modified: Tue, 17 Nov 2020 22:10:29 GMT  
		Size: 41.2 MB (41156827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d883b2b6632347781ef239b69b3566e14f83515d89658a8c8e61c10d5b8c2cc`  
		Last Modified: Tue, 17 Nov 2020 22:11:09 GMT  
		Size: 116.4 MB (116379488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ae8906dd38f6f6661b7c24aaa631e235db9edf89bb89bf65a30d288d3ee4d8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221441463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774fc33699998edf53f8d31537d952b4d28fc05d4ee30a7342e8b2e177173e26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:34 GMT
ADD file:b2545152b2d5298539a3587be3ec1f7ecfececebb4ee80eaff97f66143feac5e in / 
# Tue, 17 Nov 2020 20:21:35 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:46:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:46:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:48:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:51:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4af4a46f2c554db32c2423a35e7d1fd96ec1a41633404963392957596e60a5b`  
		Last Modified: Tue, 17 Nov 2020 20:32:10 GMT  
		Size: 50.3 MB (50305387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5e67e7f7b7f724bbb49fbc0795a7c5d76ac00b944870eb1d2ea3a69994caa`  
		Last Modified: Tue, 17 Nov 2020 22:08:52 GMT  
		Size: 16.7 MB (16723254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ae13d33a579507fdea6e1eec1193840d5da4b64759da63d75f2a9836acac9`  
		Last Modified: Tue, 17 Nov 2020 22:09:16 GMT  
		Size: 39.8 MB (39779853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed093686662704579944f5ed0aaf54c8b69c31e75b807f4d76edb19f072f6e57`  
		Last Modified: Tue, 17 Nov 2020 22:09:56 GMT  
		Size: 114.6 MB (114632969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e6f9b3387310eec820aea3e48a7c78375fa76ba9c6c29dd18419ec6c4efeb928
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254343044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdf82f0db18ce835eafa31cf92aeb320d9e201fcfaaf9efb57dcd24e0de8da4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:16 GMT
ADD file:843de10973ffdcb28448f75b968c0f3f47adc33e3bb0fa5adf1c488c8fbbf5f1 in / 
# Tue, 17 Nov 2020 20:20:16 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:09:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:12:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:17:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b79b7651073e6b6c71d7e4168850a7ded5ca4e7d948a7035975a0e83ad6703c6`  
		Last Modified: Tue, 17 Nov 2020 20:27:07 GMT  
		Size: 54.6 MB (54608823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c14b2d754487de7f15aff3e85e50a59c7af0d8f0fcd3ce1c40e8ec436e5fb2d`  
		Last Modified: Tue, 17 Nov 2020 21:25:19 GMT  
		Size: 19.9 MB (19855902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28c8c47874c59fc4e54207d922f4c54d51d7a37a316b580d7d35b07d690749`  
		Last Modified: Tue, 17 Nov 2020 21:25:38 GMT  
		Size: 44.0 MB (43991143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2585c35068181468900e9ad3aea7e9c7e386f29889eedd04b2488c2da685fe3`  
		Last Modified: Tue, 17 Nov 2020 21:26:11 GMT  
		Size: 135.9 MB (135887176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
