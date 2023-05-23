## `debian:rc-buggy`

```console
$ docker pull debian@sha256:bc6d5afc362a1938f8c5b8fa2d986afdb52b7a69603ccc57e915726589c17274
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:556730d69eeb31459c47f62a557ae5f0f186decf40af52f440102dbe294ef08d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3756f83ada75f99ec16084011ff2f41ffac0f7cb886eedb9043f7b5e8ca9d1d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:21:12 GMT
ADD file:3b942ada2dbba1c073e568411a383d6ab987c117af5bbb011afd46549d64c4dc in / 
# Tue, 23 May 2023 01:21:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:22:37 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8285c3e1284db51d7096ff9c9434e138a00153495c655a040787b10e562b7515`  
		Last Modified: Tue, 23 May 2023 01:25:36 GMT  
		Size: 49.3 MB (49289184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca62fb3224a68663c8c905585c6eb05385bcaaa302902a08cbf9114fcc2a09f0`  
		Last Modified: Tue, 23 May 2023 01:27:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:483154564a48970e5c12a396e1746485bfb6bc245df4982fc7071d460290058a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ececf4ea3db752a8bf79e9ec60707ad2250bdf5eae117483fd02e6c3acc2daf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:49 GMT
ADD file:bbdd13db0e090d7d928a2beba57e3c1340342d05e5c15f7b7377c9791a5cb4ba in / 
# Tue, 23 May 2023 00:48:50 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:49:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d14a321d144fc48aa438b2364b0f1a5667979322ef9cada9309bca48584a11a1`  
		Last Modified: Tue, 23 May 2023 00:51:36 GMT  
		Size: 47.2 MB (47154613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e3404f665334f67249172ac844a47f1e79bb25e3d0cb849f3671a54ff10585`  
		Last Modified: Tue, 23 May 2023 00:53:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:c14446c1867b4a1aed7c99003206cdad719bb142f7d27e0c8eaa5fac389c1b75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4981c49750a38199f8f6129b83a4086acf0307ff9e3c93c5e47571966b1b6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:58:50 GMT
ADD file:d575865c0ae8f8ca887a39f651f9e4f5ec16e2f0233bba91239c33ac167a8bf0 in / 
# Tue, 23 May 2023 00:58:51 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:00:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d28602ae46d2f07ea10d44c6edf1cf2be8bec1552141a793411caab17bdf1d13`  
		Last Modified: Tue, 23 May 2023 01:03:14 GMT  
		Size: 45.0 MB (44981303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ecad73e9cbd417508b5e8e109281e08c219d29cb5395fb2cad347b813f7487`  
		Last Modified: Tue, 23 May 2023 01:05:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:948ecfefda3ca8e1c8af2f2ae638e4a41e1a73612852d3ddba20551c6bf50cbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49336524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc227954a86f424939bd1883fe8b6f4ee2649b861844569c7e2c9f34d41ab881`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:48 GMT
ADD file:4608b82b211b6814e5bf372be706a6c01bd7a2a4841b59ac5430ec3a3f94468d in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:36 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5842d200e3f7df637a96b64f14e82ccb2c66e201137165f2d91447fbd3248a8c`  
		Last Modified: Tue, 23 May 2023 00:47:31 GMT  
		Size: 49.3 MB (49336298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d16b96418f665018572e36c1d3858326b529c4059b207df0620f14f598584`  
		Last Modified: Tue, 23 May 2023 00:49:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:8b7c6323d66c79f3b436846e7580f1866bf5470fdaa46df6a3a4b7f259fe62c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d52f52a0f46e1c4c785e7e7baa2c614c36bd70386aaf7303108acad34ed1801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:47 GMT
ADD file:33dd3eb2725f92170606ce015e99cc9496d244630b3f4844cb8f3f61b16e2eb0 in / 
# Tue, 23 May 2023 00:40:48 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:42:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1034171b4bde64cf8e4ff854704a3bf68000eddcceb63b481197082dced785ba`  
		Last Modified: Tue, 23 May 2023 00:46:09 GMT  
		Size: 50.3 MB (50311497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef221bf7ed0e5804a93644fffecc4abab1053075bfb0deee1cc55923e052e44d`  
		Last Modified: Tue, 23 May 2023 00:48:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:f24bee3f6a1cc054fa692448f6cfdf99c8545b1906c4f9410b824e0fb739f8a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e754dffde56ab9bc2aff2e0464f7f4edda58f0094d66a0a7efd273bd8b83b943`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:11:03 GMT
ADD file:4747b72418fe8be7c83a33927d22b74c9169c9f02959e41f61d71d739fd30ff8 in / 
# Tue, 23 May 2023 01:11:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0f1da758a33cea391a9b76cbdcea2cd41c87b5a2c179c4c1f3d65a456c65d8e1`  
		Last Modified: Tue, 23 May 2023 01:20:05 GMT  
		Size: 49.3 MB (49293333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacb7597e2e7c158018c057a11f3d14f20e3d19e914543dbd04950963c7c9695`  
		Last Modified: Tue, 23 May 2023 01:24:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:b646b65d9da68a3e55ae178a4556ad0d30f2357b2523bc3c779dda44c70334ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53302287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf629f8df7ba6dcd9adf9704be07c797a07f7c3f6d44d3555fb32fe4af711a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:52 GMT
ADD file:cffada1d28fb1dc246127e193bd218b3c76450667fe4cd380f04a5caf5571be9 in / 
# Tue, 23 May 2023 01:17:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:20:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d914d1b8acfde6dc74b2fb48f95f7aedafbe4e4ad3b6ea21aa9db007eee47739`  
		Last Modified: Tue, 23 May 2023 01:22:29 GMT  
		Size: 53.3 MB (53302061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999f4f149ecd6c0cfb1ca166596f533df165eca22ebbf89bb1cbe855106ee432`  
		Last Modified: Tue, 23 May 2023 01:25:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:84e35182aabe24cb59a5664c253dcdaf2dfc5a34ec3abcc5b5318eed2f841ee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47664842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ef5ea7483c30d687bee61eb1a2e0fd884462bdb7e86c9dfe6b118a849d3b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf18678c08e741e18d3e68d1e057a69c98ac089b51c0c6cec761803ddb321f`  
		Last Modified: Tue, 23 May 2023 00:47:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
