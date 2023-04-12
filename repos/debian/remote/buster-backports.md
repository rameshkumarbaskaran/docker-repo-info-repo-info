## `debian:buster-backports`

```console
$ docker pull debian@sha256:0c17fc243838d557622b3e7a602b3fa4a681d4ebc36e7162a75158256439eb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:e3ac5e3f77f4d5411568944cf93592832a055cfd2ddf67ae07c59d65b71f5a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e209f4e5f3d540c6aeec4f640f22517c6efef06db2dd14e9d319bc343d43c56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:20:18 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111f7e409470bbc7e49a7c71c624c7db3f51198731678f13b630aeae0921c49d`  
		Last Modified: Wed, 12 Apr 2023 00:24:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:64c7b44b0b61a1497f7c0843a14f15017b54dbfcbdb3937853eeae0d9aa7411b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e859bca7fd8cbcc1f66a62cb88c9545143170c7b8ee130f78ecc06ebb4808089`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 23:59:56 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579cccff48053a246eb15e71e198d78b3461a760b1140d0f4b159eeb17f2c673`  
		Last Modified: Wed, 12 Apr 2023 00:03:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:38909b012e9e8c35d0eab4f3338c518017fc77e1a777ae2d2b74956c778d6f1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61f55313c7fd443c984898caf97abcd0259698009e03986fcd18c489f662c39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:39:58 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891ba131a68a92f4849170a28e165e333c613ec38c29fd8cee9ae4f4a8e85456`  
		Last Modified: Wed, 12 Apr 2023 00:43:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:1681e901ae07ad9b8d7eaa38006f28b61e26a00869d29265c322a5bd4f7a6c38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1dcd56dc5f9433392d61773bae7c52793333adc286e93bcc61171c7080827a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:39:14 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf99dfccba60cad74fd547e7a78dab6288bca72a40deb3882ee89845dade1aed`  
		Last Modified: Wed, 12 Apr 2023 00:43:19 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
