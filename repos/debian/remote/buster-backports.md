## `debian:buster-backports`

```console
$ docker pull debian@sha256:c04e97cedbb4d40dce2f33854e1dd959b17761dbaa4e0a00383a89c3f9f7d5a9
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:fe99d68a7ce967cc18b46f16a1283046f577f24bfd6bd442c3f99ff9a6233fbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50436432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6fef2d0bdffde440d1a6cb7edc4bd4944cc800636f3d9361d085b793fc3a17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:22:59 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91333af859fd33749a5680b5ff4034a5b71a566b1805abe51a580812679cad64`  
		Last Modified: Tue, 28 Sep 2021 01:29:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:25b19f48f49e556b707f0d76017f83ff16fb6ca68645e33d112f5cff96be7673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc18b4d7516528b337fa6bee7117b2b64fbc22ba04927dac76bd5f5e6a916d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:58 GMT
ADD file:f9432d6da0faddeaa117c57c0c007cd56738ef01549baf71e5c59939b7e69b6c in / 
# Tue, 12 Oct 2021 00:50:59 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:51:14 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ae00de77d9c27fe3ba9ea06833b273e4fc0aa128a3a61d3992632e6e3941a78c`  
		Last Modified: Tue, 12 Oct 2021 01:07:01 GMT  
		Size: 48.2 MB (48154085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f423ff16601594ffc793510a0f613e3e31c1f522ba48ca97795cd48002054`  
		Last Modified: Tue, 12 Oct 2021 01:07:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5ffebbba4aec4cc73dd4d3f202ab16d1e05845b8b64767f9dc03f5b2c6710195
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc106bda40f34b1747d778a294f61e86f330fb2a50cc52631d5cb43764e8a55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Sep 2021 18:03:34 GMT
ADD file:da3730d9c05fab2433637063dc9d51b2505bb6023c391d606419bc9a0874c131 in / 
# Thu, 30 Sep 2021 18:03:35 GMT
CMD ["bash"]
# Thu, 30 Sep 2021 18:03:49 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d333743b3b21fdfd6ba3f4a0624204b620b72c3d0eb2c3dd9e39d23f3a87e9c`  
		Last Modified: Thu, 30 Sep 2021 18:20:10 GMT  
		Size: 45.9 MB (45917880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fef8f9196fd83ec2850acc14b8b35cc439ad0dca7cee13d7a2b0d934be2edb`  
		Last Modified: Thu, 30 Sep 2021 18:20:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7ad1dea469603f08e8ee84913b57087b230feafcc474c0350b4afdefefd8c486
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49222602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5bdf669d587a92d444e6f65df0441eb479a63d94511f7de846e15aaa6e5a96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:56 GMT
ADD file:51975e5f400da759b2cd8f7eba13ad61dd4edbbee0d0fac09b697bfa039d1515 in / 
# Tue, 28 Sep 2021 01:40:57 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:41:03 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:70fe10514d0290bd1e8986c0fd63a67204813d37fc5863cf9bf8bf61b2031537`  
		Last Modified: Tue, 28 Sep 2021 01:48:53 GMT  
		Size: 49.2 MB (49222381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2ab42436267eb7556c2d379d412f41a3c1d5b7199d8e4362c5314f44aedf1d`  
		Last Modified: Tue, 28 Sep 2021 01:49:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:9fef3b78feda90bef94916c4106072821d029e2fc2798690a484e458926b1453
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fba25d3d3be56224672a7ae9546e17914d1ca8481f7eaf9a6e2ef6dd46d090f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:28 GMT
ADD file:f0e83dd2590d6bd2d3726ebb3ebb5bfc0c2a52fe9feaeecd60b036c8eff69788 in / 
# Tue, 28 Sep 2021 01:40:28 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:40:36 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f6f6f4e486b0370ea7bec101a3770e19279a47ffd7d20a9c48000fe3e63917bc`  
		Last Modified: Tue, 28 Sep 2021 01:49:34 GMT  
		Size: 51.2 MB (51207376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7383833ae8c5a28412b13e642a6ace73d58a5cc9542ad79247c06697ddb14e`  
		Last Modified: Tue, 28 Sep 2021 01:49:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:c7de484758c2c95200f859d1152472f7e5978667cd042419dc03bd71c5da7d7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a533728c9c9a533c00930a5f61054f09e824237d89503c5a5db40b2e705192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 02:11:12 GMT
ADD file:9b5681d0673ed91672adb0ae7280c2eb5237b43c9443ab7fb11f5b521131a620 in / 
# Tue, 28 Sep 2021 02:11:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:11:18 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1654f133ae6b958f64c6efae84c28a80b40fcb50eb467b706a5e8376aa40e7cb`  
		Last Modified: Tue, 28 Sep 2021 02:21:29 GMT  
		Size: 49.1 MB (49079722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5cd2f9ec199a8011881aa2fd984976274fd44ad8fb6d7d7829deb1d409d18d`  
		Last Modified: Tue, 28 Sep 2021 02:21:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a30de89d9832f78149b3eaf310cc7565ffbd4ac3b0d9670f53f5be4db725669b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998830489111058fb2594943007feec48fd536b12158472d8eb395adde814f95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 04 Oct 2021 17:55:26 GMT
ADD file:50366e64986438ff4c350e35a97f65653448dfef465d9dafa6457b580265c545 in / 
# Mon, 04 Oct 2021 17:55:35 GMT
CMD ["bash"]
# Mon, 04 Oct 2021 17:55:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b69bfcd37d02e2d93198e38015f28e42ae522cd1eb09e5d8110d51bc3f25a6fe`  
		Last Modified: Mon, 04 Oct 2021 18:07:59 GMT  
		Size: 54.2 MB (54182947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1277a1c6baaf2c8c833725a17c9d9076326738c3dcffefe821450f27adfffb`  
		Last Modified: Mon, 04 Oct 2021 18:08:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:c80ce30bb6f35fb54f41e085e04c040ed61461c819e3e1efc37abb9a7eb3032f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc2b4826ca9a3909fa5023a43d0e660b997461b2ed25e9170741ed622d59978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:39 GMT
ADD file:91e4bb81a5308737580259a9213b02933901431aa2ea23f3f4f59321a6ccc301 in / 
# Tue, 12 Oct 2021 00:42:41 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:42:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9df790508568720a3b71c02b057e4a119d9d2e8ed003ccba18d600e1ea44fa8a`  
		Last Modified: Tue, 12 Oct 2021 00:48:22 GMT  
		Size: 49.0 MB (49004847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cf9091035162137105954527ad7088a181db3c9efb679b91bc6a8189807b01`  
		Last Modified: Tue, 12 Oct 2021 00:48:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
