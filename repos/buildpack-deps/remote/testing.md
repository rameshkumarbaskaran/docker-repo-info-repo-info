## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:142fd015663047d4d3402a623d3f2313f0912fd020810aa343b6534cf6d50fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:06ca0b1dddc945f1302013c074d94311cd9e78af4f68049d9d334f8fda23ec4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348618379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6599a671025c141a6b461bded858b59991f7e705d588e7800ba76b056a145be1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:19:36 GMT
ADD file:aea4560c39a3a877086fc63afdf218ba3600a05abef7c44563f788e8b60c04ef in / 
# Tue, 23 May 2023 01:19:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:45:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:47:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c98dda1b0e97e7fa61fa33cea43f85bb1a36a4f6f65c7b8430cae442b76ece09`  
		Last Modified: Tue, 23 May 2023 01:23:14 GMT  
		Size: 49.3 MB (49301275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a463ac54ed3eeee295443fb87b28643b95d7975e83bd214bc93db462b1b59de`  
		Last Modified: Tue, 23 May 2023 01:55:08 GMT  
		Size: 24.3 MB (24274092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7076663891554c4b6516ec84fd2d5459502966e94b4d794796b086aea4f4ca2`  
		Last Modified: Tue, 23 May 2023 01:55:24 GMT  
		Size: 64.1 MB (64107344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcc83cd0070aac1337a07c643595a04962dde075826e954f6a5a2c0e2cfa82d`  
		Last Modified: Tue, 23 May 2023 01:55:56 GMT  
		Size: 210.9 MB (210935668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:45042aff5955087fb42e7926e5083662816560e204c9ff9af10b2ef86b86a776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338618864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63d0113d6c9154f0b72cbd751734f94e9b70d06b00c11d2ae26092f46e40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 01:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dfbc5e6b18e516ad072378c62dcfa42e9981f0925b16c44303b5c7f6424eca`  
		Last Modified: Sat, 26 Aug 2023 02:00:57 GMT  
		Size: 62.3 MB (62298697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76154f4b1c42c402e154efcbbb3b3594eaa5766589d7938250f678a4ccbc7bac`  
		Last Modified: Sat, 26 Aug 2023 02:01:34 GMT  
		Size: 208.7 MB (208674771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4425189a5d13f4eed8516313b4737c64abc895fae6178e11a6291a176b657d8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301360882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d7c03dd45bb5ecdb71536af0285c1a4d02af39e79b87337cbe0d2c7e4a373`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:57:23 GMT
ADD file:76738dad56d76cef0c57f5c574260e6494d397ba6ea95f5ea14ceeda292e8a0d in / 
# Tue, 23 May 2023 00:57:23 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:51:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:54:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b62ba7ac5fd70caec3910c292af59431036e6a2f6a4fc4266b3c04d3f6f7febd`  
		Last Modified: Tue, 23 May 2023 01:00:49 GMT  
		Size: 45.0 MB (44989913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5316b360a91afe489f52f8edacb51535faca57922a648164ceab10593e7842`  
		Last Modified: Tue, 23 May 2023 10:03:35 GMT  
		Size: 22.2 MB (22176633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d1443969900c81509f08727255738a226e326b2e78357a9f564ed1a40e0de`  
		Last Modified: Tue, 23 May 2023 10:03:56 GMT  
		Size: 59.3 MB (59257052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9627394e509dea2f0f30066bdeae5b06de7f19598ce28bfbf4a5db5165fc67c6`  
		Last Modified: Tue, 23 May 2023 10:04:34 GMT  
		Size: 174.9 MB (174937284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cec27f8a93f3d172775d3288cfaec8b4b769f65e0a7ee6a3c68e2118f8e60397
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339505547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5778655674135dc99c990b6d810a6c09e98e16a1015143472ecadd13a18fa98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:54 GMT
ADD file:91184714f613e1768e87fad722350f471376a88cb595664e8e23864ce5d79071 in / 
# Tue, 23 May 2023 00:42:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:52:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:54:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3485dc61c38c6db2e8092e9f4326fe6c51e867a1841f55346f74ec25847d7401`  
		Last Modified: Tue, 23 May 2023 00:45:14 GMT  
		Size: 49.3 MB (49347785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f929165e3c93f5d762267d93e97574e2fd7ebf4c98f33a2664ca58afb970b9a`  
		Last Modified: Tue, 23 May 2023 06:02:01 GMT  
		Size: 23.8 MB (23810063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cce032e95f3ca3e3210588e183ef0e95a0ab610151c718bf68d1f7f497f4a9`  
		Last Modified: Tue, 23 May 2023 06:02:17 GMT  
		Size: 64.0 MB (63985159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924469098fdac134f558d7447f87168e7d9583cf37707ed9c1116b72c3ea318`  
		Last Modified: Tue, 23 May 2023 06:02:45 GMT  
		Size: 202.4 MB (202362540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3d0aa40e31daf90f34882c964a7e88bf77f7ba88105a0b77218e52eec3077468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351278231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70893e3a566643fb18e37fe78bc6a178372ea9a8888b1a4621f8398b437ea51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:38:43 GMT
ADD file:4d14207b5cf935fa2b9de70132f41a0eb90a8b5200ed3d27e60b766fc6131e13 in / 
# Tue, 23 May 2023 00:38:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:54:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22e40771358829b6817b47cb2d682b51257385478c18bb1ec96251a68a9c75e4`  
		Last Modified: Tue, 23 May 2023 00:43:23 GMT  
		Size: 50.3 MB (50323189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008bf109a603c637e9a80a5a8fe46353089a5fb8c6333eced350af89d7298576`  
		Last Modified: Tue, 23 May 2023 02:03:46 GMT  
		Size: 25.1 MB (25110482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39204aa4c310e5b428093f5182d87e2f302dabb686c85507aed2372505156242`  
		Last Modified: Tue, 23 May 2023 02:04:08 GMT  
		Size: 66.0 MB (65969876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489790d665a9caa11ab395ed735a1f587a230f693c4468d6ee11b6b885e5259c`  
		Last Modified: Tue, 23 May 2023 02:04:53 GMT  
		Size: 209.9 MB (209874684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5fa5e52436ba17dab736dbf38e4a5f8a017c28d54c6fea2f362a687c51ff422d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325659093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81324403f6259df61fcb3d3d0521221ffd1820d0f103881ab60f89a81b7be660`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:07:59 GMT
ADD file:c8965d5e1a440e4bc93318be2f80c95e9692ada237122031d2e98793b8036143 in / 
# Tue, 23 May 2023 01:08:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:48:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65775e721f6c7f76e54f65c03408a249103c86c536e6a86498f9f5a6229b9f4e`  
		Last Modified: Tue, 23 May 2023 01:17:24 GMT  
		Size: 49.3 MB (49304239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464924f070f4f4c8a4e8facea0026336e200a0c517951d62854dc3b3a1154f58`  
		Last Modified: Tue, 23 May 2023 02:06:54 GMT  
		Size: 23.9 MB (23864351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f2eaa37862504aa49ac76cb23ed1f915f986e4579bc54affd5a7e8ab8f277`  
		Last Modified: Tue, 23 May 2023 02:07:44 GMT  
		Size: 62.9 MB (62948637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542a3d9567799a39308da784e60aa90d7b75c46dba25dd189fec72c7040a50b`  
		Last Modified: Tue, 23 May 2023 02:09:49 GMT  
		Size: 189.5 MB (189541866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8a505e6a396f5f035dcbea2cf46d4bf41c257478b4e9329f0e1fdfe5e17bf53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362786127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5942d86ca7e84bea64a7b2e9c57641bb32edc3da17a4328ef6facefdf6814015`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:16:38 GMT
ADD file:28e774b3554d274fc742feac48f78a3bf6f120cb729e2824007dd94d5c414156 in / 
# Tue, 23 May 2023 01:16:40 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:46:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e109feef3fc6307cd9a880958cef6624de9c2c6f054987e479461a1ae51c7503`  
		Last Modified: Tue, 23 May 2023 01:20:49 GMT  
		Size: 53.3 MB (53312324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab84a55cc084469df8b38ab6a01658bfba2b29b7410a970ba6d9d2864846672`  
		Last Modified: Tue, 23 May 2023 01:59:19 GMT  
		Size: 25.9 MB (25923867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfbe0bc6dc85168e7da83a7be20c9913921338417e0c639a93ff1cdc5664403`  
		Last Modified: Tue, 23 May 2023 01:59:46 GMT  
		Size: 69.6 MB (69566996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab2c83c92e0bca392c1c98be8c27bf6a116f567d39ba305e515f7e3f013e2bc`  
		Last Modified: Tue, 23 May 2023 02:00:44 GMT  
		Size: 214.0 MB (213982940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b418603fa1312cefd9f98f374d44fa9eaf2276b3cfd3c081b60bc372cfb29c74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318075990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec6dc3c068aa2ffd814452ea011310362b305e830f6eb7d6630c484ce7ad1f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:04 GMT
ADD file:cc95a0712a6bccebd449eb4ff979eeed054299ca9b7766e545c76d0c23c957ee in / 
# Tue, 23 May 2023 00:42:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:32:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:32:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ffb123da88ae28227159c41b0f21826f6497089ece0b790a5c14d890cf50771`  
		Last Modified: Tue, 23 May 2023 00:45:12 GMT  
		Size: 47.7 MB (47673474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3541e04aeeb82d496c085951f9619fcdf7bce92b4b7185f684cbb7ef6f65ea32`  
		Last Modified: Tue, 23 May 2023 02:37:57 GMT  
		Size: 24.3 MB (24270889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984494917df72746bed1d04a989f9f1cf3cbeeef990a9d0a58690373ab6ffaf`  
		Last Modified: Tue, 23 May 2023 02:38:13 GMT  
		Size: 63.1 MB (63110310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41017c83158d69d524990028b820ba0d40fd774ba21cc0643ce36e5378d1fc45`  
		Last Modified: Tue, 23 May 2023 02:38:39 GMT  
		Size: 183.0 MB (183021317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
