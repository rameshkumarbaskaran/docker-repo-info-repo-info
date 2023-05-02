## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:23cf38ea578aae80305b3d9b605c26354ca64f7009a5e7f9d54d4f17a6ce67e5
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:3950fa6c3d923f7929c4e08231d72abaee40420cc7798d78c823a161c2cbf0f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55052961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72e890b198a7f9ae8a9907a7f5950cf254bd7c658e9980e88bf9c69c5f74800`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:19:59 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd102085f0f28e20f71187d0f003b7d02edd9a13fdee8001aad360df3ca94df`  
		Last Modified: Wed, 12 Apr 2023 00:23:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:eb6d3e1e4d0e1f835be420b48a537a82f367827db57a89698f834581fae9c363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52546757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f13fee9ad9733a747fc6bad922bf7125275767d91b5fcbd65057e24ca7357e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:48:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1827544a6fedf0f8c24aa3074567b30472563d25dfc99582e13dc3bfa2bfa793`  
		Last Modified: Tue, 02 May 2023 22:51:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:63e41b11b53d39265994fb5b1b81c43ed0d49320a92f27d5a47ef1ecf4306e0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50217110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a3d84d0562e2dbcdf040560adbc51181885f294e5f6e9a1bff941f68a92814`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 23:59:38 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809a1996a22b675eefd3fce9f8b70de051d1433a66b77748d11c2d18115e8a4d`  
		Last Modified: Wed, 12 Apr 2023 00:03:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ef0569c515bdcfeb3fb0b31a7e6ef72ef0d331286431cbe658a21daec2e2d671
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68f5a36ebe060459bae2685b263bdc37cd7e3000bf600b658fe3985c7c45591`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:39:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50f79822c1334542a2c647bbf2e495cf662e6e25e976764bc9a86e51b6c3411`  
		Last Modified: Wed, 12 Apr 2023 00:42:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:fdcfa7ec57f1bbad816752c0acbd7b49f0163fe243db03def156128a17d9e7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56033044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc77a4ac31486b1355dd091e5132ed1f8ceb5f6c28964699dcdcc5215e2b5a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:38:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163cbf4c07d8e1ed01c72bdfbbc181381fa7346b0c7d7873d513877905cc0dad`  
		Last Modified: Wed, 12 Apr 2023 00:42:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6bba04ef78172e50a76a1adeae6948d95da13d2b10947194a1e133be255246e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82192e5ae21def8646a916631d34811734eb115466795c16169066406cdb4574`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:09:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c557479b9edd028d1b34e5256f9070b200d4fce958cf9e84613c83dea79c0`  
		Last Modified: Wed, 12 Apr 2023 00:17:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0dcf75aa727af3bf39e300f0e936e662682d6243c4e67f3701c9d00501bd3654
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58926827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5edd0906c02fc00f201665e4a5b81026c9c7dec72fca0b3a17050d22791895`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:08:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78baafc7df2db64930490d209b66bee4bd2f7845f03591a93f95be17fe677f1`  
		Last Modified: Wed, 12 Apr 2023 00:12:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:0e4c0a91f063aa664e5393b1c602a2121fef4fdc1b375e6bac354961019eb77c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53286910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55d666fcb5965f2338b94392975cb40f61b7a40d568169be8f119d160f5bca9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:00:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5f8ea362068477a4e1f3dc8e71b20734f89fdc76fa216834c78d37b4ff337c`  
		Last Modified: Wed, 12 Apr 2023 00:05:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
