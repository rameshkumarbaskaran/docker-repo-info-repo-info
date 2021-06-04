<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20210421.0`](#amazonlinux20202104210)
-	[`amazonlinux:2.0.20210421.0-with-sources`](#amazonlinux20202104210-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20210521.1`](#amazonlinux2018030202105211)
-	[`amazonlinux:2018.03.0.20210521.1-with-sources`](#amazonlinux2018030202105211-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:99cace8a34eab4093b1e0d12f1c21b1c04989808ff5864ef4ca62cc6b2a5d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:930034b169a5d135367a750be2bb7ecf2d6eff2283b74fc7125c22668fad9a92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61947132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef897d731f9a5673c083d0e86d7911f85d6e63bb2be2346b17bdbacdc58637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c0bff228592a826f1984cf0ee7dcfa9666a4684cbc0d2a5c59d7c1dcd97ad38a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63660068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d6b5e6158e74da5bcb33d989cff6140bc313ad70996b28c65e7d40b1a4c748`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:92a93194e51ae2b7bca16cc13d23ed8d24f1ff654292721a95ef2fd4a794d8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:54a81a819385e5ba38b4586b3c960265d106ef7c3924e123dc6848a5b4c8c797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542818467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4415525a0de6b386eda3d2e8e55c3530698cf3846bd4fda077e8e21743635d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:26:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa16be21b849cedc18925697d377825ff62903ab864293be050e3af75e2de4`  
		Last Modified: Thu, 29 Apr 2021 22:28:00 GMT  
		Size: 480.9 MB (480871335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:22ae10d8afcfbc828545f5925e7b7fb66201f45664b4def51f22b9c64b6481ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544531395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc6f6ea121d17b21f32bcfa7f650c13201914dc60ca0e269e86adbffd7134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 21:39:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d087798acb0c72603bd5a19518ad85996bbcc1faa1951c260238b894cec0b`  
		Last Modified: Thu, 03 Jun 2021 21:40:41 GMT  
		Size: 480.9 MB (480871327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210421.0`

```console
$ docker pull amazonlinux@sha256:99cace8a34eab4093b1e0d12f1c21b1c04989808ff5864ef4ca62cc6b2a5d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210421.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:930034b169a5d135367a750be2bb7ecf2d6eff2283b74fc7125c22668fad9a92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61947132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef897d731f9a5673c083d0e86d7911f85d6e63bb2be2346b17bdbacdc58637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210421.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c0bff228592a826f1984cf0ee7dcfa9666a4684cbc0d2a5c59d7c1dcd97ad38a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63660068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d6b5e6158e74da5bcb33d989cff6140bc313ad70996b28c65e7d40b1a4c748`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210421.0-with-sources`

```console
$ docker pull amazonlinux@sha256:92a93194e51ae2b7bca16cc13d23ed8d24f1ff654292721a95ef2fd4a794d8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210421.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:54a81a819385e5ba38b4586b3c960265d106ef7c3924e123dc6848a5b4c8c797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542818467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4415525a0de6b386eda3d2e8e55c3530698cf3846bd4fda077e8e21743635d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:26:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa16be21b849cedc18925697d377825ff62903ab864293be050e3af75e2de4`  
		Last Modified: Thu, 29 Apr 2021 22:28:00 GMT  
		Size: 480.9 MB (480871335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210421.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:22ae10d8afcfbc828545f5925e7b7fb66201f45664b4def51f22b9c64b6481ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544531395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc6f6ea121d17b21f32bcfa7f650c13201914dc60ca0e269e86adbffd7134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 21:39:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d087798acb0c72603bd5a19518ad85996bbcc1faa1951c260238b894cec0b`  
		Last Modified: Thu, 03 Jun 2021 21:40:41 GMT  
		Size: 480.9 MB (480871327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:99cace8a34eab4093b1e0d12f1c21b1c04989808ff5864ef4ca62cc6b2a5d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:930034b169a5d135367a750be2bb7ecf2d6eff2283b74fc7125c22668fad9a92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61947132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef897d731f9a5673c083d0e86d7911f85d6e63bb2be2346b17bdbacdc58637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c0bff228592a826f1984cf0ee7dcfa9666a4684cbc0d2a5c59d7c1dcd97ad38a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63660068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d6b5e6158e74da5bcb33d989cff6140bc313ad70996b28c65e7d40b1a4c748`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:92a93194e51ae2b7bca16cc13d23ed8d24f1ff654292721a95ef2fd4a794d8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:54a81a819385e5ba38b4586b3c960265d106ef7c3924e123dc6848a5b4c8c797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542818467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4415525a0de6b386eda3d2e8e55c3530698cf3846bd4fda077e8e21743635d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:26:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa16be21b849cedc18925697d377825ff62903ab864293be050e3af75e2de4`  
		Last Modified: Thu, 29 Apr 2021 22:28:00 GMT  
		Size: 480.9 MB (480871335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:22ae10d8afcfbc828545f5925e7b7fb66201f45664b4def51f22b9c64b6481ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544531395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc6f6ea121d17b21f32bcfa7f650c13201914dc60ca0e269e86adbffd7134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 21:39:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d087798acb0c72603bd5a19518ad85996bbcc1faa1951c260238b894cec0b`  
		Last Modified: Thu, 03 Jun 2021 21:40:41 GMT  
		Size: 480.9 MB (480871327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
