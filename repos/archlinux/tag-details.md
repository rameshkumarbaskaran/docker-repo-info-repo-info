<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20221204.0.107760`](#archlinuxbase-202212040107760)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20221204.0.107760`](#archlinuxbase-devel-202212040107760)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:55c45738d156c99d00242e830ec54eef8c02748a7c2dbe248892da9a1205974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3d6aee337dd9ecc8fe77748b2ca752fd8df376bb7906e12c78df405fc67e59cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141795991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8792549afc11a8564693e63f6d1a75a45d0c24b76f288b4a9030ffa0dcb8b1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:20:00 GMT
COPY dir:4757859b63a669f0999e7e839d9752a4922ec2fb682fc9d4736e5e0dca4a7504 in / 
# Mon, 05 Dec 2022 20:20:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:20:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b4eb00ee61960c4be31f11880595238c7a8821317aa5768f85ee62d5c4d26685`  
		Last Modified: Mon, 05 Dec 2022 20:21:42 GMT  
		Size: 141.8 MB (141788039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00026c6783148c69ad6afbc1f14108341d55e2944decd384eeccc93693bbc508`  
		Last Modified: Mon, 05 Dec 2022 20:21:22 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20221204.0.107760`

```console
$ docker pull archlinux@sha256:55c45738d156c99d00242e830ec54eef8c02748a7c2dbe248892da9a1205974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20221204.0.107760` - linux; amd64

```console
$ docker pull archlinux@sha256:3d6aee337dd9ecc8fe77748b2ca752fd8df376bb7906e12c78df405fc67e59cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141795991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8792549afc11a8564693e63f6d1a75a45d0c24b76f288b4a9030ffa0dcb8b1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:20:00 GMT
COPY dir:4757859b63a669f0999e7e839d9752a4922ec2fb682fc9d4736e5e0dca4a7504 in / 
# Mon, 05 Dec 2022 20:20:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:20:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b4eb00ee61960c4be31f11880595238c7a8821317aa5768f85ee62d5c4d26685`  
		Last Modified: Mon, 05 Dec 2022 20:21:42 GMT  
		Size: 141.8 MB (141788039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00026c6783148c69ad6afbc1f14108341d55e2944decd384eeccc93693bbc508`  
		Last Modified: Mon, 05 Dec 2022 20:21:22 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:67bc73f3952a7fa0e63c83a6fc0a218adb95d4e9925db100cf8e717efc50596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:76bd5cb87f5e7cec03196249530ead7404b154507f677fdc2572d0b296aef95a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242990004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76159f99df5f82cbfcdb27a95f4dc8b6386f011851d5a61cf14ee374a53e494`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:21:01 GMT
COPY dir:e1c43c82e176f0ee5255fc4df29ca1cd8a31ad1955dd4d2c0b4b1063f039c1d0 in / 
# Mon, 05 Dec 2022 20:21:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:21:04 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:21:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c52c4b627283e2c5bbf333053262dc5d8c615f4877d4f124c1c39be5d62706c3`  
		Last Modified: Mon, 05 Dec 2022 20:22:29 GMT  
		Size: 243.0 MB (242981363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2858aab8a1ab92eb25a7112696e5233d3336e057e3c273719e17007efb6402df`  
		Last Modified: Mon, 05 Dec 2022 20:21:53 GMT  
		Size: 8.6 KB (8641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20221204.0.107760`

```console
$ docker pull archlinux@sha256:67bc73f3952a7fa0e63c83a6fc0a218adb95d4e9925db100cf8e717efc50596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221204.0.107760` - linux; amd64

```console
$ docker pull archlinux@sha256:76bd5cb87f5e7cec03196249530ead7404b154507f677fdc2572d0b296aef95a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242990004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76159f99df5f82cbfcdb27a95f4dc8b6386f011851d5a61cf14ee374a53e494`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:21:01 GMT
COPY dir:e1c43c82e176f0ee5255fc4df29ca1cd8a31ad1955dd4d2c0b4b1063f039c1d0 in / 
# Mon, 05 Dec 2022 20:21:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:21:04 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:21:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c52c4b627283e2c5bbf333053262dc5d8c615f4877d4f124c1c39be5d62706c3`  
		Last Modified: Mon, 05 Dec 2022 20:22:29 GMT  
		Size: 243.0 MB (242981363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2858aab8a1ab92eb25a7112696e5233d3336e057e3c273719e17007efb6402df`  
		Last Modified: Mon, 05 Dec 2022 20:21:53 GMT  
		Size: 8.6 KB (8641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:55c45738d156c99d00242e830ec54eef8c02748a7c2dbe248892da9a1205974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3d6aee337dd9ecc8fe77748b2ca752fd8df376bb7906e12c78df405fc67e59cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141795991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8792549afc11a8564693e63f6d1a75a45d0c24b76f288b4a9030ffa0dcb8b1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:20:00 GMT
COPY dir:4757859b63a669f0999e7e839d9752a4922ec2fb682fc9d4736e5e0dca4a7504 in / 
# Mon, 05 Dec 2022 20:20:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:20:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b4eb00ee61960c4be31f11880595238c7a8821317aa5768f85ee62d5c4d26685`  
		Last Modified: Mon, 05 Dec 2022 20:21:42 GMT  
		Size: 141.8 MB (141788039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00026c6783148c69ad6afbc1f14108341d55e2944decd384eeccc93693bbc508`  
		Last Modified: Mon, 05 Dec 2022 20:21:22 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
