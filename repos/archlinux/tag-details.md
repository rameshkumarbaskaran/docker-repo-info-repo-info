<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20221113.0.102112`](#archlinuxbase-202211130102112)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20221113.0.102112`](#archlinuxbase-devel-202211130102112)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:dbbca0130b8c3e7510253cd92cfdcf3f28598a349a9930cefff6cc45021cb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e719a261315bba5921531d42b0d6674257cd4fc3bd6dc73da195be51f00ceb46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141800558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ac09d64eb0928c684311308d508b38a3d5651c1747e3cd4d123a09e5b3f2a4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:20:05 GMT
COPY dir:0b29e8a8a5a9fd93fb5f5e2d98404d2c5f608767e46b908bf4971f318050ae65 in / 
# Mon, 14 Nov 2022 21:20:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:20:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:66f1918ed3645cee708501fdf5ad4165722b681578838a6e2a3ecc62d6356b1b`  
		Last Modified: Mon, 14 Nov 2022 21:21:48 GMT  
		Size: 141.8 MB (141792615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb266927e885e2141d3da730e8342dba72c2a027ca011a504a85a6c6477057a6`  
		Last Modified: Mon, 14 Nov 2022 21:21:27 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20221113.0.102112`

```console
$ docker pull archlinux@sha256:dbbca0130b8c3e7510253cd92cfdcf3f28598a349a9930cefff6cc45021cb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20221113.0.102112` - linux; amd64

```console
$ docker pull archlinux@sha256:e719a261315bba5921531d42b0d6674257cd4fc3bd6dc73da195be51f00ceb46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141800558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ac09d64eb0928c684311308d508b38a3d5651c1747e3cd4d123a09e5b3f2a4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:20:05 GMT
COPY dir:0b29e8a8a5a9fd93fb5f5e2d98404d2c5f608767e46b908bf4971f318050ae65 in / 
# Mon, 14 Nov 2022 21:20:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:20:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:66f1918ed3645cee708501fdf5ad4165722b681578838a6e2a3ecc62d6356b1b`  
		Last Modified: Mon, 14 Nov 2022 21:21:48 GMT  
		Size: 141.8 MB (141792615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb266927e885e2141d3da730e8342dba72c2a027ca011a504a85a6c6477057a6`  
		Last Modified: Mon, 14 Nov 2022 21:21:27 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:ce6fcd78c698176b06f81cf2d1f881ca86f5fbc6b6078894af42a1fe1ea170df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4e96b5361c605ef460c2cc315370e809b227634da51a7d49abb8fa9c32ca4044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243005615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d090529544b8276299fa5979b7d7960828752afd4a5182ca64d4b71519302e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:21:06 GMT
COPY dir:8c06a6373ab1904938712a4232a2a4b86ecbb85293114557f3dccf4c2c6c23c3 in / 
# Mon, 14 Nov 2022 21:21:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:21:09 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:21:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:81811940900b378cdf21a67573dea207571aeece75a017e6e12ba2629b65e64c`  
		Last Modified: Mon, 14 Nov 2022 21:22:34 GMT  
		Size: 243.0 MB (242997003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb557f22bcc7268e490cabcc90e6ff57290814121c7f4d979047f8045a0639`  
		Last Modified: Mon, 14 Nov 2022 21:21:58 GMT  
		Size: 8.6 KB (8612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20221113.0.102112`

```console
$ docker pull archlinux@sha256:ce6fcd78c698176b06f81cf2d1f881ca86f5fbc6b6078894af42a1fe1ea170df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221113.0.102112` - linux; amd64

```console
$ docker pull archlinux@sha256:4e96b5361c605ef460c2cc315370e809b227634da51a7d49abb8fa9c32ca4044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243005615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d090529544b8276299fa5979b7d7960828752afd4a5182ca64d4b71519302e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:21:06 GMT
COPY dir:8c06a6373ab1904938712a4232a2a4b86ecbb85293114557f3dccf4c2c6c23c3 in / 
# Mon, 14 Nov 2022 21:21:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:21:09 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:21:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:81811940900b378cdf21a67573dea207571aeece75a017e6e12ba2629b65e64c`  
		Last Modified: Mon, 14 Nov 2022 21:22:34 GMT  
		Size: 243.0 MB (242997003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb557f22bcc7268e490cabcc90e6ff57290814121c7f4d979047f8045a0639`  
		Last Modified: Mon, 14 Nov 2022 21:21:58 GMT  
		Size: 8.6 KB (8612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:dbbca0130b8c3e7510253cd92cfdcf3f28598a349a9930cefff6cc45021cb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e719a261315bba5921531d42b0d6674257cd4fc3bd6dc73da195be51f00ceb46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141800558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ac09d64eb0928c684311308d508b38a3d5651c1747e3cd4d123a09e5b3f2a4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:20:05 GMT
COPY dir:0b29e8a8a5a9fd93fb5f5e2d98404d2c5f608767e46b908bf4971f318050ae65 in / 
# Mon, 14 Nov 2022 21:20:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:20:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:66f1918ed3645cee708501fdf5ad4165722b681578838a6e2a3ecc62d6356b1b`  
		Last Modified: Mon, 14 Nov 2022 21:21:48 GMT  
		Size: 141.8 MB (141792615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb266927e885e2141d3da730e8342dba72c2a027ca011a504a85a6c6477057a6`  
		Last Modified: Mon, 14 Nov 2022 21:21:27 GMT  
		Size: 7.9 KB (7943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
