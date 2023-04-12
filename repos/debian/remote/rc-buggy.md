## `debian:rc-buggy`

```console
$ docker pull debian@sha256:578bf3761decc0294fe1e42aeb46754c753cf717e3bef8fbec91aba4fa4e9bca
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
$ docker pull debian@sha256:d35a285fb08b8722c07733c192753d398cbe27590ee8b4899a4ec18dcb89c88c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49287880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b09361a3f014b9ffdc3988e728b61cd4862f45deee0905f2acf4e9cb37377e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edf299448d12355c6805ac3c08f004fef53f15385eb953042929a3ec684674d`  
		Last Modified: Wed, 12 Apr 2023 00:27:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:453ab545ff54779788a519060d180e3ad8c7bd58906ff0f8a038015babb88b51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be659aabd4da5007dfcfd64ce57640483468ea57340a62ef1e0a4ca6fb73a73c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:49:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75d93d939c318fe4fdba16185fa42737f41ce94348161485ec517ab2c3d9c1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b0ebe70634e0c690afff84a11f8eb8a4ab1158fc78f3f6109cfb139e06652c9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45890460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa9c73cd8469f68b83f4ce921fd4f4719d0071f8fd6958ec57132313f9cecfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:01:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652d2c86befd540f1eda8dfebd2efd59357820a8cf7865b7e11580c20e62e14e`  
		Last Modified: Wed, 12 Apr 2023 00:06:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:82d2f7ee13ac76334c78b2f3c96b1c7efb42a61b3904420f9f2a49afe6076ef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49327880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cfd69d0e398ecc7f50f3385676047333f44629583783f25e7dbe8bf5352de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:41:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04bd62d44ba32e027825f8869408c8b0295c49fe85344680d94abf86db6c6d6`  
		Last Modified: Wed, 12 Apr 2023 00:45:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:03d4bda50d596a59a92288cafdae6af75c5d0fc9db31a5b46bfe0eac99d415d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9a5f3e5bde0c62a30d57edf3500a9cbbe67582306843836074927296b6baa6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:41:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cb04deba2a42338f73109b3337e09edf3604bfe0c5e9f19f674937a58cd4f`  
		Last Modified: Wed, 12 Apr 2023 00:46:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4efaac374daf67a00881479de182296dbfbaf2c645a1e8d3efeccf06d0d22c71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49296476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edba465505f792b976470866a4803f97d60b35b3769d87cbad1db198fda4bfb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:14:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897bc05f3645d90b6207202f6d835e763d3053e4c7de843cd7cb9ab95bfb932f`  
		Last Modified: Wed, 12 Apr 2023 00:22:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:d4519be529428ab720a44d25f5dd9f20c1104599d223a81d68e63f17e3a53998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53291936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c6bb2b7533ed8946304bee172ef4de94ab95a47dce6d325e6c6bcacc21994c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:11:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631ed35ea15d9ffd6a47c821d9f697df2fea786ea2e328c6911a1dbc8cb8ee22`  
		Last Modified: Wed, 12 Apr 2023 00:16:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:34880ad087f8d44ade019bc181ba20dbedfcee313ff1bc5958b92ffecdffda62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47665294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b26e192406c0b2ffdc0c2fd405a8026f126defd65a4dcba5f0140832bf08c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:04:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61f1a1750709a627c6e075515fb08a8ba057dc062a5f19ab977db129e84ef86`  
		Last Modified: Wed, 12 Apr 2023 00:06:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
