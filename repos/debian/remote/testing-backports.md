## `debian:testing-backports`

```console
$ docker pull debian@sha256:505f0630b52956d4fa3ce60029ee7dd742fbfddb6dbe6a58834a102496b35fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:1d9ea76a0070f7cf106dba2b4b714008fb707b73353f3f079d8209071f5ae260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51852930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d3d27c9a3c9fd7d1bc6e060b3a4358a6772b49a91530becd3ddcfe5a141825`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:54 GMT
ADD file:bf9b71c3da178fa1ba282c110853082e94e9f8a90773b43b6104bdb8c9e54f5a in / 
# Wed, 26 Feb 2020 00:41:54 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:42:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1fcd5305bc72cb154c6bf3d1a204b8bcfc0d91d4811e6681dd2b7aafdaaa8669`  
		Last Modified: Wed, 26 Feb 2020 00:47:41 GMT  
		Size: 51.9 MB (51852708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67e7a6834b1a54301feed22e9d193d7055644b9de4baa8e488285971ce3cb9`  
		Last Modified: Wed, 26 Feb 2020 00:47:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3811afa08da0d6a1def0e98c763ef76479b5880f18ce436c5248d8d61a9f0dfe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49859666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7a5c47a32cf4fd0d00a41808a71253f40c6762c5e9ab2a7c1e4300927f577e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:54:18 GMT
ADD file:ac01181c8365ede8cc9aafbc68fbf8a106070c95386d375bb2fff94194015f82 in / 
# Wed, 26 Feb 2020 00:54:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:55:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d55adb79e59138108e397d3445e8279cd4c12a787370372aaae8d74303bd1184`  
		Last Modified: Wed, 26 Feb 2020 01:04:01 GMT  
		Size: 49.9 MB (49859441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca95fba5454c390a97d774a4beeb13de82da623ca81eec9853766753cc4ee5e`  
		Last Modified: Wed, 26 Feb 2020 01:04:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0402633911c27e86afea4875a64a8e24965c8edc31edaef0b0d6526e87a14ec7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47581498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa949252b0f354a010118a8e39286d5710cd6c9fab2ace4bf53e3e63fc6caf4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:02:00 GMT
ADD file:77b2cdf50e357f756539c8263b5b078f294cbbcbaa77472bbc9aac630840e2fa in / 
# Wed, 26 Feb 2020 01:02:04 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:02:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a7d8964a2b313bf0c932514e37d93c1b7e653e39445154fd2a2b97229b5f3f2`  
		Last Modified: Wed, 26 Feb 2020 01:12:10 GMT  
		Size: 47.6 MB (47581274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b144577a5b2482bf9b291edff61a12030572c404743fb5a9dbf32fcd187c4`  
		Last Modified: Wed, 26 Feb 2020 01:12:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:357ec9ee94e4c74997acfa58411369cf86fdca27cbebd3725f56477ff1fd2c25
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50808722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc7e2ccd6bcedfea31bf7386adb2004a854c5d1a1c84436c8ad2ebda747ff3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:51:35 GMT
ADD file:e032e27e8935ad66dc76d8dd15bdf9fb36fcc0318c7e322fcdae2ee219c11b61 in / 
# Wed, 26 Feb 2020 00:51:42 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:52:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c55f06ecbc45a6b3fd4dcd737b73d5b6baa8545548d0610d133fad7fbb7be09e`  
		Last Modified: Wed, 26 Feb 2020 00:59:19 GMT  
		Size: 50.8 MB (50808498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c329d6552bdfd56db1bd2205ac320b3980e5124ccafddc8f561e6fbd8694f41d`  
		Last Modified: Wed, 26 Feb 2020 00:59:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:963d14545f88d4a69659eb062df1e4d52643f802c373ac4b35c9acff94275036
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53002939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77a260fd035fca570df79e3184d44ecde389e00b9e2637b2b1d1abf8823e3a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:35:59 GMT
ADD file:9a37eb812440af2fa6bb9b53caf4fcbba9d6c709edc69f1fe2b2f47195abee7f in / 
# Wed, 26 Feb 2020 00:35:59 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:36:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:713e3f76a9b5faa14362eec3ae0c403aeb49a616a1003367b73392ff5eb46faf`  
		Last Modified: Wed, 26 Feb 2020 00:42:22 GMT  
		Size: 53.0 MB (53002719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c41cdc9c7e1e576985a4ee3a6265f916416bdc3f4c99d1bf6209af849b3a5`  
		Last Modified: Wed, 26 Feb 2020 00:42:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f3cee84fb3717c56746d609b7f4e9c21902f56ccb61dbc89846ad499b7e43db3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55696824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761ee2d460c5dfb6a84155ccb1606dc8e3d805c1b0593666a1fea9e80badb292`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:38:01 GMT
ADD file:0dbef65592e778c76e0dd94a65bcf63def0e10cec3d3ae266289cd65a6eccc60 in / 
# Wed, 26 Feb 2020 01:38:08 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:38:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:753c26ee271df27f66edda54cb118118829aac536238586c0edc363a9662c220`  
		Last Modified: Wed, 26 Feb 2020 02:06:19 GMT  
		Size: 55.7 MB (55696598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1782355573b8392918f12fa4d72c8b35b78bbcbd205834107f8378515efcfa9e`  
		Last Modified: Wed, 26 Feb 2020 02:06:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:a7ef9bd73a1cb632a57b78b736933c84168c26ff7af96c82855ce049e3baa2fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3c20edae68cc23f20e6f86f4412d6b3816abd1ebff400402cf1cfdb0bb1a2a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:45:12 GMT
ADD file:35c9c67c243d6ee981113893297c9f91610abc3f4f8fc695e712d1bf5e7991c1 in / 
# Wed, 26 Feb 2020 00:45:21 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:45:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa3ec75d7f3cf53cae07836c22db68711638d2fbdb74aea08833d90eb47e6f75`  
		Last Modified: Wed, 26 Feb 2020 00:49:36 GMT  
		Size: 50.5 MB (50483673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cf34b0fbb8c89aaa6bf692b2458ecf1ea138a2b2c57c4deb710d98a1f9e3ce`  
		Last Modified: Wed, 26 Feb 2020 00:49:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
