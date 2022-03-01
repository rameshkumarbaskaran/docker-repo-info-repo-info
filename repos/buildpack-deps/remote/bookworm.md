## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:dec01c2f5e2d8650c2916f2106b1c11f13a92dd36f29b212eaa16b8f7492c5dd
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

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e1bdfb7b1ef283972d3445e885a1e09a59e7161837dd49b26057b8f109595ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332187006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c234031eecdd72a069f263966d0ff59c6aca4d2e810a780b94cbe15cdf70cb72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:48 GMT
ADD file:ba00d13bcd1098159b17d28658733d14360751081a0ff0ae5e599ea2b24d8bfb in / 
# Tue, 01 Mar 2022 02:12:49 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:24:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:24:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:25:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e0d8da139e3fe03100d4937bc5abe5a82000a26ba213987f21c101384e663b3`  
		Last Modified: Tue, 01 Mar 2022 02:18:16 GMT  
		Size: 55.8 MB (55764122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d860ac80d90a3973e603f905ad5187aa30b4c4bc1166661080e7b5d70eb9b7`  
		Last Modified: Tue, 01 Mar 2022 06:34:57 GMT  
		Size: 5.3 MB (5275155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439be32a1f7086d86d5df8e4bc94c4e6afe93efcf848747f2a0414cf45ba26e2`  
		Last Modified: Tue, 01 Mar 2022 06:34:58 GMT  
		Size: 10.9 MB (10915420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55bfedab5c66617cbef5e27ef99e597f5fa0d602ff494db70a20d8d483d24ec`  
		Last Modified: Tue, 01 Mar 2022 06:35:17 GMT  
		Size: 57.0 MB (56975332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9894d63f2dcbb3d2642ed6d129d3ab8cf3b31f2ef0bfb75c2bfcfab98707c26c`  
		Last Modified: Tue, 01 Mar 2022 06:36:01 GMT  
		Size: 203.3 MB (203256977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f60147abdd7df4b130c24264396a0c44cab96b0dd593bd5e89958e2be00796d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303166590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab52e75a6a450afab9a24c0a84da2af5322d01454c966ffd4012d1ab53dee1a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:15 GMT
ADD file:1c7800709331eb899ffb3adab213dd035f158fbb5682366917ca9b29bca0df53 in / 
# Tue, 01 Mar 2022 02:01:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:56:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:57:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 02:58:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:00:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73894112358cdc16a19d6f8dc64e5d28dbe24c82ac6079e97e3750913f71a9bd`  
		Last Modified: Tue, 01 Mar 2022 02:16:26 GMT  
		Size: 53.2 MB (53159389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85671ba5fc3ddadb093aa6d64a5f20d876e7de8441908798eb76d8ae77670100`  
		Last Modified: Tue, 01 Mar 2022 03:21:22 GMT  
		Size: 5.2 MB (5174924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d9a4597c4c1fcff57e018f1450613480d9459062fbda983eb61aacf9903cc`  
		Last Modified: Tue, 01 Mar 2022 03:21:24 GMT  
		Size: 10.6 MB (10582879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236207ccfaed595b8a0b1f8a30a1a773ffa5152b875797d1784012fe3214b79`  
		Last Modified: Tue, 01 Mar 2022 03:22:15 GMT  
		Size: 54.6 MB (54604486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edea6003139fe9d9f51047a5a0e6fffac65952fcc583d307eccc7ec00ec33e3`  
		Last Modified: Tue, 01 Mar 2022 03:24:15 GMT  
		Size: 179.6 MB (179644912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acbae2409d8ee8c88d0ef960365f776aee8a450548fa9b0506605f212a4aeaba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290124154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179997a54dca706a98fa38181b757a38c71db6c7f7aaad3ab4079fce4e889381`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:09 GMT
ADD file:b4dba23a3881b51ce93a5fac275db003c57e88fc4534625e4c57917ee7d15dad in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:25:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bac975da179fd2ec964b1f0a2374ae27456aefbe28014e1301872aaa7a545619`  
		Last Modified: Tue, 01 Mar 2022 02:17:11 GMT  
		Size: 50.8 MB (50787576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c6337247740872b2c547fe2c235240cb511f34f377358193108cc09d66ea1`  
		Last Modified: Tue, 01 Mar 2022 09:48:05 GMT  
		Size: 5.0 MB (5035170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1747c607a3fe8511a51023b984fd817a06b714e0a09c5028257ed90eebc47b0f`  
		Last Modified: Tue, 01 Mar 2022 09:48:06 GMT  
		Size: 10.2 MB (10241471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d3fa20637f40c1c0d555bbe24b09ee9dfe45ffa828cf0a24e2e432278157`  
		Last Modified: Tue, 01 Mar 2022 09:48:54 GMT  
		Size: 52.5 MB (52465949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b00a72b43e8f3657d5e5c9aaffd0cbaea84db01532fa5c55196727a6e494c`  
		Last Modified: Tue, 01 Mar 2022 09:50:41 GMT  
		Size: 171.6 MB (171593988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1405882e794ed421625db80b3131ded15cde2fe6d3082122472eba14c44393b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324694080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5a353f2901977182c8b280e5ef00e125f27ec2a50a60b6f425f5f26c12d7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:47 GMT
ADD file:6cc6cb40b70acca2462997590c41a6b84b7434e382c9b14ee43a22dcd7981979 in / 
# Tue, 01 Mar 2022 02:10:47 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:31:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:31:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:33:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ef7b4e27074d58d976b796a4f016999e5977498dbef83e6266727f3bedc89af`  
		Last Modified: Tue, 01 Mar 2022 02:17:12 GMT  
		Size: 54.7 MB (54704495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc4f4f700543c2cb8f09a5e25cea55c5087ffce8b003613f3eab3bcacac0eec`  
		Last Modified: Tue, 01 Mar 2022 10:43:20 GMT  
		Size: 5.3 MB (5263173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eb0c886efc88379b75421a9b2e06041df5838818e786ffa383c74457975d62`  
		Last Modified: Tue, 01 Mar 2022 10:43:20 GMT  
		Size: 10.7 MB (10676648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578936971e5991e696d98d5a7f536e4949c9238980f0811a672e74a9e494eb49`  
		Last Modified: Tue, 01 Mar 2022 10:43:39 GMT  
		Size: 57.0 MB (57004768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc986d4be7efdb8eb7fbc44dc3e9fc7029ce53fa4e7b833290688a7fe605e967`  
		Last Modified: Tue, 01 Mar 2022 10:44:14 GMT  
		Size: 197.0 MB (197044996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a148537ee74a0833c7a74556b6aa468858213de93497f17740debc1b8c86dab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335605243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83222059d3e7d2dc975d0b07c14bc99d3b0e1acad226e01ff2cd04b8756071d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:44 GMT
ADD file:2e2ec9677737b8bd29e3af438e4f72a00e4024d7771df47c835bc532f3955901 in / 
# Tue, 01 Mar 2022 02:06:44 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86f9569b4496bcb71f9a06eca983db008f228f89df9115b51deb7ba67bce86ba`  
		Last Modified: Tue, 01 Mar 2022 02:14:26 GMT  
		Size: 56.8 MB (56800248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc642b9c58ccfd6d24ba39de754790979cb5f4259049a1024063ce9ecd8048b3`  
		Last Modified: Tue, 01 Mar 2022 05:50:18 GMT  
		Size: 5.4 MB (5407350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03eabfe59d42c8a3ee934b6d80db7f1185e56951d5ec5a9561133731b6ff2d`  
		Last Modified: Tue, 01 Mar 2022 05:50:19 GMT  
		Size: 11.3 MB (11307416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf25e617660ac5db1f4151bbb260abc3f5330b37a67e7d43f48b6f5966bbb024`  
		Last Modified: Tue, 01 Mar 2022 05:50:45 GMT  
		Size: 58.4 MB (58393620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76570adf4796e6a45c9f30952a2243bd7ff6a21a66e4b0950f9434ad5b02150f`  
		Last Modified: Tue, 01 Mar 2022 05:51:41 GMT  
		Size: 203.7 MB (203696609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:055adb463397355ab524867765537a61d3338809ee2528a5bbe76f5e2d287253
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312929677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f354c4cfa4c4510d2efac12e774d3bf4f200ba2861f5ffb9486e200c2094ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:16 GMT
ADD file:205e6fa10b349b94cd09f9ab81d41ac5b9cc551f15798915ab0db37a758e13ed in / 
# Tue, 01 Mar 2022 02:01:16 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:58:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 02:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:03:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f016bfd811ef5b25e78858421fa083872f3db557018c6de8e9e19a3db5d69e73`  
		Last Modified: Tue, 01 Mar 2022 02:10:17 GMT  
		Size: 54.4 MB (54412288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1db773d06493b0e4fe3289f2a2bab8a332145545a6d356ae31f7c1daeda745`  
		Last Modified: Tue, 01 Mar 2022 03:18:13 GMT  
		Size: 5.2 MB (5232019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55060d22611a46bff620b26ad27b1ccccea40ec3d18f5f2fb5712efa15c5b9d`  
		Last Modified: Tue, 01 Mar 2022 03:18:15 GMT  
		Size: 10.9 MB (10874821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95190bbea2f5622f90e93b782a17ea09bf555524c1063b8108ca896c2dbd1b8a`  
		Last Modified: Tue, 01 Mar 2022 03:19:01 GMT  
		Size: 55.8 MB (55783298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d57a0a2810b75bdd63fac199f873c7c02629ee17b47387d0c94dcb85e250896`  
		Last Modified: Tue, 01 Mar 2022 03:21:03 GMT  
		Size: 186.6 MB (186627251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a5b8c298ba9fc35f9ffdbabf625761780304d6737bb7749489de6050f84b714a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342348288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3ca3a84d07b37a19d27cd4ce709aec3e0910f507b867a820b225f1552f8233`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:22 GMT
ADD file:08a06b615cc3142b45e95ffc03be0940c1aed49581fdb5c3a45d69c9ba65fcdf in / 
# Tue, 01 Mar 2022 02:03:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:55:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:05:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e0578def7e304114d931a4e4be85f40364b30cf0228e8360d7ec9d82b30f2519`  
		Last Modified: Tue, 01 Mar 2022 02:13:53 GMT  
		Size: 60.2 MB (60166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb379d336c1a24b02d5693d3a19fe1017d67c67f734a56c109c876bcf8547f99`  
		Last Modified: Tue, 01 Mar 2022 07:40:40 GMT  
		Size: 5.5 MB (5543531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a933c5a043de953ab3d5444edf590034fecf2a41084159c2ff91dcb57e349a89`  
		Last Modified: Tue, 01 Mar 2022 07:40:41 GMT  
		Size: 11.7 MB (11693203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0f79d5cc50dad2e31cae3c2ec67b9cfde06f4ead1e7e8f99141438474a7ff1`  
		Last Modified: Tue, 01 Mar 2022 07:41:06 GMT  
		Size: 61.7 MB (61676232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fc6ac6727fc8844e30486d606a1aab7f1a7cb8b264218aa5521ff271c2db5`  
		Last Modified: Tue, 01 Mar 2022 07:41:51 GMT  
		Size: 203.3 MB (203268957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ed5db6953401c7e699848b7694ee5f369308c3e2b4b6e72f6f5ec3bab7badc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304469056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7b1cea4d98d05e3a0be9e16f118b90fd9d51e75bb6086f7108175fc48d3d46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:03 GMT
ADD file:97ccc226b81c90fe178edd1d68832f3a504aa1ef983753f12fed36e4fa09c796 in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:49:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:50:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d7c29f1e9903c84021327567eb513269c7f0b92b6f050037783556a33deac133`  
		Last Modified: Tue, 01 Mar 2022 02:06:47 GMT  
		Size: 54.0 MB (54007195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed9e936b2203a39badf459e13626bb8073e325e33067ce97b014c0f2564b7be`  
		Last Modified: Tue, 01 Mar 2022 03:59:12 GMT  
		Size: 5.3 MB (5256848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11b370eba2faadba4103ab569fe90fa51ac4c8f6634d504e481540d47ad92f7`  
		Last Modified: Tue, 01 Mar 2022 03:59:12 GMT  
		Size: 10.8 MB (10807240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d45193a064820414c9ad891c79c41aeec7b351b45dfe7bb4c3631e05a9b1ca1`  
		Last Modified: Tue, 01 Mar 2022 03:59:26 GMT  
		Size: 56.4 MB (56362036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea71a8a91b0ea5860e608ef124f417b70e0f75853ad98e50b7d871c8b387be12`  
		Last Modified: Tue, 01 Mar 2022 03:59:51 GMT  
		Size: 178.0 MB (178035737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
