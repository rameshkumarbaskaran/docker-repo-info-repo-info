<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20230308`](#ubuntubionic-20230308)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230412`](#ubuntufocal-20230412)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230308`](#ubuntujammy-20230308)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230412`](#ubuntukinetic-20230412)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230415`](#ubuntulunar-20230415)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:8aa9c2798215f99544d1ce7439ea9c3a6dfd82de607da1cec3a8a2fae005931b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:0779371f96205678dbcaa3ef499be2e5f262c8b09aadc11754bf3daf9f35e03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941d3b032a8168d53508410a67baad120a563df67a7959565a30a1cb2114731`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5227665c11379f79e9da3d3e4f1724f9316b87d259ac0131628ca1b923a392`  
		Last Modified: Wed, 08 Mar 2023 03:59:25 GMT  
		Size: 25.7 MB (25688211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:715ddeafc950876ef9451c460d43ac1ba3e90655f582d845c7f656ee557bd2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0feaeaa2e651a8712ecfc0727458ba88952949b4b9136d20f0e7adb6a743c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55e299352d1e9c6f1d6e7aee23f9204c8e147eec9fb877be5649ad7f1af58bca`  
		Last Modified: Wed, 08 Mar 2023 03:59:37 GMT  
		Size: 21.4 MB (21394593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e77e90f3a41b2c9480c68088c746065623ba9ca77f4e311070ebf404ac6ef2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1adc1968c7b7646687f8585de8e3473681323cb9052956ed8f509529a52e61d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13f679bb266a0be5756ce3bb145f89ccd6395d778b1a4bed5a0b0b26105bde2b`  
		Last Modified: Wed, 08 Mar 2023 03:59:31 GMT  
		Size: 22.7 MB (22710750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:7cbc4fafddce3cf793a94c3b5dc6295a3f569b9222c5e4e74b38aa00a65442fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713953b7d565f057a079026363b57bd30e4e9fef8aeaf217f6c4c8b20d968f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:472741f7e602c0ee1b34eaf14bb55e0a9377b9f28b0b00fd7ddb5b9d07046a7d`  
		Last Modified: Wed, 08 Mar 2023 03:59:42 GMT  
		Size: 26.1 MB (26095131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c955620556f7490d6c4cbd7c1d73faeaad2f635cc3207ee8278832c897d1a7e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45b2835cf4d380d116f2d5e52053a8335089236b194c117adf34efac0409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:293f1b6b3486ffa5f90fdcf0f22fc2091718a3e012fadf073bf57b6a8604df20`  
		Last Modified: Wed, 08 Mar 2023 03:59:48 GMT  
		Size: 29.4 MB (29350183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:1e8deff80e7d247c13e32a88efe3ca7314c2e8eb6ab5224e1a7671d7d8076428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed683baf1b6cc5ec9754e58ee88c3414d4781d2b27d33dc89e16d191249bd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff61d052565af59dfea677d587c19bf7759efb08fa5db9c11019e2b30b183d9b`  
		Last Modified: Wed, 08 Mar 2023 03:59:54 GMT  
		Size: 24.7 MB (24743830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:a2a8d2816944af4f5119a2037ad348e69de944556b0ca93e8ef1f3cd14aeedf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:223d6beaf1aa0978b7a0dc4731333b59fe35ee9d3a8c48db1a8d686b1b211ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4731390bddee2b1dc9fa35d820d20b69f95bb16381ae1434821f52eb87f9d503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3503cc1332f3fe649c8a0937dbf6f052f1d2d9b9bdb97546cf15f09ec495d7a4`  
		Last Modified: Wed, 08 Mar 2023 05:10:41 GMT  
		Size: 23.6 MB (23608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f92b9de5f10b6e1fcda653f5d02bd6c816386dfb830c71cef95df52b2280cd1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625d192afcdc5add2f097cd05a177ab19f18e69473911dbb479fc5eba56ba8fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a774dfcdedc7c7c4f0009ddadc2f33557d60452450684534df5625f9693df81a`  
		Last Modified: Wed, 08 Mar 2023 05:10:35 GMT  
		Size: 26.0 MB (25973169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ee77c5eb098846cf57a751c5b4d28678f152ebd936ee700570f77e5181f94749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae7691e3a999c7848a0952ef29ffbb1c235587dfce87cba0df7e8d23a8b0be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:58 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:42:00 GMT
ADD file:4463dafd3352de8c5ff87090e2f30be9bdffc3fa9d84e27b13e2364d856f82e9 in / 
# Wed, 08 Mar 2023 04:42:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68e65db8d2065c8b6d0764029cabc60b7c7bfd9dc8fb638e0effa6e544486597`  
		Last Modified: Wed, 08 Mar 2023 05:10:53 GMT  
		Size: 26.4 MB (26364051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:67211c14fa74f070d27cc59d69a7fa9aeff8e28ea118ef3babc295a0428a6d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:7a57c69fe1e9d5b97c5fe649849e79f2cfc3bf11d10bbd5218b4eb61716aebe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d22c0ceb150ddeb2237c5fa3129c0183f3cc6f5eeb2e7aa4016da3ad02140a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2ab09b027e7f3a0c2e8bb1944ac46de38cebab7145f0bd6effebfe5492c818b6`  
		Last Modified: Wed, 08 Mar 2023 05:10:20 GMT  
		Size: 29.5 MB (29533950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ad18cfdb19dac67bf0072dacea661a817330e5c955d081f4d09914e743ae5d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf0095935ffb29018664cf219d8c1b2c890e3e3c4af89113df23e7330397187`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aea1895b7fd03ef3bc263eef4b6f1dd219fc3286f3ff79495aadb81a88650723`  
		Last Modified: Wed, 08 Mar 2023 05:10:33 GMT  
		Size: 26.1 MB (26140319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:537da24818633b45fcb65e5285a68c3ec1f3db25f5ae5476a7757bc8dfae92a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8ce5c00ca3ef91e0d3eb4c6e6d6ec7cffa9574c447fd8d54a8d96e7c1c80e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd741b12a7eaa64357041c2d3f4590c898313a7f8f65cd1577594e6ee03a8c38`  
		Last Modified: Wed, 08 Mar 2023 05:10:27 GMT  
		Size: 27.3 MB (27347481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f23b7ade9f88f91c8d5932a48b721712ed509a607d9a05cdeae4cd06de09e5f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220c61b3ab7b82dd3ff3395f9efe2b63e730c3f24284d1519013cf3cda822f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2561b3b559ec9b25bafa07804afa433803291265f7dd847de711224b0f238237`  
		Last Modified: Wed, 08 Mar 2023 05:10:39 GMT  
		Size: 34.6 MB (34593661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:b351315d950a4da70f19d62f4da5dd7f9a445eb8c8d6851a5b6cdddbdafb13cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad39053efde0c294433cd8f9709c6d69a36e1f0af4ffbf81c3d261caffb615`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:15f635e04e894b7646b4ebca40424ddf244867fc663429ea8b877eca172a7cf1`  
		Last Modified: Wed, 08 Mar 2023 05:10:46 GMT  
		Size: 28.0 MB (28015959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:4a6ce3cbf8ca08ffec2e69ec71a0635664d2911a2d5985f9e44d2a264e756706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e37c01607a81ee7737f164af67cb5f5f8e1ecbf82c4f5cfe940675b8e8830ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bcbf2021edfcf5671a4872ded2d62d36cd3a86813acc7bc2471fefce3c2ac2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:55:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:55:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:55:49 GMT
ADD file:827330b6c59e67c5d2edd3ceb3492b97865b15f9246f14710f478d12e94d2048 in / 
# Wed, 08 Mar 2023 05:55:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c09adf37dd1d92aeedd2906b2635d9b7f1eca9f39f51d52f919d26d113c8d35`  
		Last Modified: Wed, 08 Mar 2023 06:38:49 GMT  
		Size: 25.1 MB (25067205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a79f91eb2bb4ffc5d96c58a06fda63550bf94a1a6b2e9ef2f835e52ca8a04ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25760037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c48db988d0f48de4461bb2bf49524880c28c5863b1ba5b175a9d7c284b009`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:57:57 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:57:58 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:57:59 GMT
ADD file:884e00dc91bf6d392fa3d117913cc2534177128322d89137bfb8b2734bc38579 in / 
# Wed, 08 Mar 2023 05:58:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f720bb411d1d3a6b6c043988c66cdaeee655f968c6eabf7f1ada7ac1529b046`  
		Last Modified: Wed, 08 Mar 2023 06:38:43 GMT  
		Size: 25.8 MB (25760037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:c69324f895a9152b8a80f9d310710a9d2ef987330d04bc20dbfe23e79e5183bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997349fe1813d9306e1ad38084ecc78950e221fe4f75cd9a85e5213139fcd80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 06:11:04 GMT
ARG RELEASE
# Wed, 08 Mar 2023 06:11:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 06:11:06 GMT
ADD file:974d67ca1d5bcaacbc707820609d36af0d7ed3ff7179a702a4aa56dcc43f79f3 in / 
# Wed, 08 Mar 2023 06:11:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e7f1a81217015da9b8db635ad002e08952988dc4100cbec474290e8524391920`  
		Last Modified: Wed, 08 Mar 2023 06:39:01 GMT  
		Size: 25.5 MB (25488878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:87cb4adffc1badb17b483120780cafc4ae0c7558e463a604c911dd38762f8483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f18a21d414ad3c0a8eea08fec8f98d730c5c02ddb0d5fef9c60ca72ac53329c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c92df8590c370b0dcf10c9273b5c18a74e08fb6089ae37d4ad9590fbdecc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cdca6f9f82cb2f31168afd36307721605cb5f89b51b97fa630583843ddb624a4`  
		Last Modified: Sat, 15 Apr 2023 05:20:43 GMT  
		Size: 26.8 MB (26825187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e685540e6030c9b728fa6485ca8e844d824e064c9a790bc54e6e6507974ba42e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24559160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4ad84aaa1e06e217b7ed880b9bea183f12a02bb5b8408f57855354fbd91c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 18:18:28 GMT
ARG RELEASE
# Tue, 14 Mar 2023 18:18:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 18:18:30 GMT
ADD file:dc39df38ee577fc1ddb753815787f9a90231d34a28c65e14298d136132c8d7d5 in / 
# Tue, 14 Mar 2023 18:18:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec8b1962079f6d8d8477e2e227966fcf2e91d26a81735eb5f0411f84cbf8740`  
		Last Modified: Tue, 14 Mar 2023 18:47:12 GMT  
		Size: 24.6 MB (24559160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b864a1f0e9f2686fcaa86491f78d38af1b9e8e53e965df39d991a8b685bf7c74
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26007489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e399e758a4b24fbecd3eed7dbaadf0eb3aa45f2ee4b2c133561693f31008b42b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:38:32 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:38:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:38:40 GMT
ADD file:2562122b72f2bcdd0678a1bd0836dcbf376a8e33078452497d85ed0cd425391f in / 
# Tue, 14 Mar 2023 17:38:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff6383e8c55f097496fc03e31f40ad77007ac50d51f9735a1d45789985087387`  
		Last Modified: Tue, 14 Mar 2023 18:47:06 GMT  
		Size: 26.0 MB (26007489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:1840997cef13af4d355cf1b5bda18e68073cc6aefe673bd36cb93ea91f3452a2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25634517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6744e3a8d8d30ea66143d1d2ba080a6cb9a9e1356857de142edfd33ddefb5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:47:18 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:47:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:47:20 GMT
ADD file:1ed4a1aa279c8c4fd49f73ed214f53835caecef222778b80716ba71fe60cc7f0 in / 
# Tue, 14 Mar 2023 17:47:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de8d2f62d0190fb3786c431d236f8d6178a12304755c3c13b8c1ff4d6097587f`  
		Last Modified: Tue, 14 Mar 2023 18:47:26 GMT  
		Size: 25.6 MB (25634517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:8aa9c2798215f99544d1ce7439ea9c3a6dfd82de607da1cec3a8a2fae005931b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:0779371f96205678dbcaa3ef499be2e5f262c8b09aadc11754bf3daf9f35e03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941d3b032a8168d53508410a67baad120a563df67a7959565a30a1cb2114731`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5227665c11379f79e9da3d3e4f1724f9316b87d259ac0131628ca1b923a392`  
		Last Modified: Wed, 08 Mar 2023 03:59:25 GMT  
		Size: 25.7 MB (25688211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:715ddeafc950876ef9451c460d43ac1ba3e90655f582d845c7f656ee557bd2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0feaeaa2e651a8712ecfc0727458ba88952949b4b9136d20f0e7adb6a743c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55e299352d1e9c6f1d6e7aee23f9204c8e147eec9fb877be5649ad7f1af58bca`  
		Last Modified: Wed, 08 Mar 2023 03:59:37 GMT  
		Size: 21.4 MB (21394593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e77e90f3a41b2c9480c68088c746065623ba9ca77f4e311070ebf404ac6ef2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1adc1968c7b7646687f8585de8e3473681323cb9052956ed8f509529a52e61d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13f679bb266a0be5756ce3bb145f89ccd6395d778b1a4bed5a0b0b26105bde2b`  
		Last Modified: Wed, 08 Mar 2023 03:59:31 GMT  
		Size: 22.7 MB (22710750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:7cbc4fafddce3cf793a94c3b5dc6295a3f569b9222c5e4e74b38aa00a65442fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713953b7d565f057a079026363b57bd30e4e9fef8aeaf217f6c4c8b20d968f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:472741f7e602c0ee1b34eaf14bb55e0a9377b9f28b0b00fd7ddb5b9d07046a7d`  
		Last Modified: Wed, 08 Mar 2023 03:59:42 GMT  
		Size: 26.1 MB (26095131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c955620556f7490d6c4cbd7c1d73faeaad2f635cc3207ee8278832c897d1a7e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45b2835cf4d380d116f2d5e52053a8335089236b194c117adf34efac0409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:293f1b6b3486ffa5f90fdcf0f22fc2091718a3e012fadf073bf57b6a8604df20`  
		Last Modified: Wed, 08 Mar 2023 03:59:48 GMT  
		Size: 29.4 MB (29350183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:1e8deff80e7d247c13e32a88efe3ca7314c2e8eb6ab5224e1a7671d7d8076428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed683baf1b6cc5ec9754e58ee88c3414d4781d2b27d33dc89e16d191249bd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff61d052565af59dfea677d587c19bf7759efb08fa5db9c11019e2b30b183d9b`  
		Last Modified: Wed, 08 Mar 2023 03:59:54 GMT  
		Size: 24.7 MB (24743830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic-20230308`

```console
$ docker pull ubuntu@sha256:8aa9c2798215f99544d1ce7439ea9c3a6dfd82de607da1cec3a8a2fae005931b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20230308` - linux; amd64

```console
$ docker pull ubuntu@sha256:0779371f96205678dbcaa3ef499be2e5f262c8b09aadc11754bf3daf9f35e03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941d3b032a8168d53508410a67baad120a563df67a7959565a30a1cb2114731`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5227665c11379f79e9da3d3e4f1724f9316b87d259ac0131628ca1b923a392`  
		Last Modified: Wed, 08 Mar 2023 03:59:25 GMT  
		Size: 25.7 MB (25688211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230308` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:715ddeafc950876ef9451c460d43ac1ba3e90655f582d845c7f656ee557bd2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0feaeaa2e651a8712ecfc0727458ba88952949b4b9136d20f0e7adb6a743c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55e299352d1e9c6f1d6e7aee23f9204c8e147eec9fb877be5649ad7f1af58bca`  
		Last Modified: Wed, 08 Mar 2023 03:59:37 GMT  
		Size: 21.4 MB (21394593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230308` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e77e90f3a41b2c9480c68088c746065623ba9ca77f4e311070ebf404ac6ef2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1adc1968c7b7646687f8585de8e3473681323cb9052956ed8f509529a52e61d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13f679bb266a0be5756ce3bb145f89ccd6395d778b1a4bed5a0b0b26105bde2b`  
		Last Modified: Wed, 08 Mar 2023 03:59:31 GMT  
		Size: 22.7 MB (22710750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230308` - linux; 386

```console
$ docker pull ubuntu@sha256:7cbc4fafddce3cf793a94c3b5dc6295a3f569b9222c5e4e74b38aa00a65442fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713953b7d565f057a079026363b57bd30e4e9fef8aeaf217f6c4c8b20d968f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:472741f7e602c0ee1b34eaf14bb55e0a9377b9f28b0b00fd7ddb5b9d07046a7d`  
		Last Modified: Wed, 08 Mar 2023 03:59:42 GMT  
		Size: 26.1 MB (26095131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230308` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c955620556f7490d6c4cbd7c1d73faeaad2f635cc3207ee8278832c897d1a7e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45b2835cf4d380d116f2d5e52053a8335089236b194c117adf34efac0409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:293f1b6b3486ffa5f90fdcf0f22fc2091718a3e012fadf073bf57b6a8604df20`  
		Last Modified: Wed, 08 Mar 2023 03:59:48 GMT  
		Size: 29.4 MB (29350183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230308` - linux; s390x

```console
$ docker pull ubuntu@sha256:1e8deff80e7d247c13e32a88efe3ca7314c2e8eb6ab5224e1a7671d7d8076428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed683baf1b6cc5ec9754e58ee88c3414d4781d2b27d33dc89e16d191249bd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff61d052565af59dfea677d587c19bf7759efb08fa5db9c11019e2b30b183d9b`  
		Last Modified: Wed, 08 Mar 2023 03:59:54 GMT  
		Size: 24.7 MB (24743830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:87cb4adffc1badb17b483120780cafc4ae0c7558e463a604c911dd38762f8483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f18a21d414ad3c0a8eea08fec8f98d730c5c02ddb0d5fef9c60ca72ac53329c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c92df8590c370b0dcf10c9273b5c18a74e08fb6089ae37d4ad9590fbdecc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cdca6f9f82cb2f31168afd36307721605cb5f89b51b97fa630583843ddb624a4`  
		Last Modified: Sat, 15 Apr 2023 05:20:43 GMT  
		Size: 26.8 MB (26825187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e685540e6030c9b728fa6485ca8e844d824e064c9a790bc54e6e6507974ba42e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24559160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4ad84aaa1e06e217b7ed880b9bea183f12a02bb5b8408f57855354fbd91c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 18:18:28 GMT
ARG RELEASE
# Tue, 14 Mar 2023 18:18:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 18:18:30 GMT
ADD file:dc39df38ee577fc1ddb753815787f9a90231d34a28c65e14298d136132c8d7d5 in / 
# Tue, 14 Mar 2023 18:18:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec8b1962079f6d8d8477e2e227966fcf2e91d26a81735eb5f0411f84cbf8740`  
		Last Modified: Tue, 14 Mar 2023 18:47:12 GMT  
		Size: 24.6 MB (24559160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b864a1f0e9f2686fcaa86491f78d38af1b9e8e53e965df39d991a8b685bf7c74
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26007489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e399e758a4b24fbecd3eed7dbaadf0eb3aa45f2ee4b2c133561693f31008b42b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:38:32 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:38:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:38:40 GMT
ADD file:2562122b72f2bcdd0678a1bd0836dcbf376a8e33078452497d85ed0cd425391f in / 
# Tue, 14 Mar 2023 17:38:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff6383e8c55f097496fc03e31f40ad77007ac50d51f9735a1d45789985087387`  
		Last Modified: Tue, 14 Mar 2023 18:47:06 GMT  
		Size: 26.0 MB (26007489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:1840997cef13af4d355cf1b5bda18e68073cc6aefe673bd36cb93ea91f3452a2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25634517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6744e3a8d8d30ea66143d1d2ba080a6cb9a9e1356857de142edfd33ddefb5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:47:18 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:47:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:47:20 GMT
ADD file:1ed4a1aa279c8c4fd49f73ed214f53835caecef222778b80716ba71fe60cc7f0 in / 
# Tue, 14 Mar 2023 17:47:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de8d2f62d0190fb3786c431d236f8d6178a12304755c3c13b8c1ff4d6097587f`  
		Last Modified: Tue, 14 Mar 2023 18:47:26 GMT  
		Size: 25.6 MB (25634517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:a2a8d2816944af4f5119a2037ad348e69de944556b0ca93e8ef1f3cd14aeedf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:223d6beaf1aa0978b7a0dc4731333b59fe35ee9d3a8c48db1a8d686b1b211ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4731390bddee2b1dc9fa35d820d20b69f95bb16381ae1434821f52eb87f9d503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3503cc1332f3fe649c8a0937dbf6f052f1d2d9b9bdb97546cf15f09ec495d7a4`  
		Last Modified: Wed, 08 Mar 2023 05:10:41 GMT  
		Size: 23.6 MB (23608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f92b9de5f10b6e1fcda653f5d02bd6c816386dfb830c71cef95df52b2280cd1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625d192afcdc5add2f097cd05a177ab19f18e69473911dbb479fc5eba56ba8fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a774dfcdedc7c7c4f0009ddadc2f33557d60452450684534df5625f9693df81a`  
		Last Modified: Wed, 08 Mar 2023 05:10:35 GMT  
		Size: 26.0 MB (25973169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:ee77c5eb098846cf57a751c5b4d28678f152ebd936ee700570f77e5181f94749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae7691e3a999c7848a0952ef29ffbb1c235587dfce87cba0df7e8d23a8b0be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:58 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:42:00 GMT
ADD file:4463dafd3352de8c5ff87090e2f30be9bdffc3fa9d84e27b13e2364d856f82e9 in / 
# Wed, 08 Mar 2023 04:42:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68e65db8d2065c8b6d0764029cabc60b7c7bfd9dc8fb638e0effa6e544486597`  
		Last Modified: Wed, 08 Mar 2023 05:10:53 GMT  
		Size: 26.4 MB (26364051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230412`

```console
$ docker pull ubuntu@sha256:d1b07a32ad33fc130e37e5c9d690dc85ddeb145c6a3c5129642247aa8c427415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `ubuntu:focal-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:67211c14fa74f070d27cc59d69a7fa9aeff8e28ea118ef3babc295a0428a6d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:7a57c69fe1e9d5b97c5fe649849e79f2cfc3bf11d10bbd5218b4eb61716aebe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d22c0ceb150ddeb2237c5fa3129c0183f3cc6f5eeb2e7aa4016da3ad02140a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2ab09b027e7f3a0c2e8bb1944ac46de38cebab7145f0bd6effebfe5492c818b6`  
		Last Modified: Wed, 08 Mar 2023 05:10:20 GMT  
		Size: 29.5 MB (29533950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ad18cfdb19dac67bf0072dacea661a817330e5c955d081f4d09914e743ae5d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf0095935ffb29018664cf219d8c1b2c890e3e3c4af89113df23e7330397187`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aea1895b7fd03ef3bc263eef4b6f1dd219fc3286f3ff79495aadb81a88650723`  
		Last Modified: Wed, 08 Mar 2023 05:10:33 GMT  
		Size: 26.1 MB (26140319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:537da24818633b45fcb65e5285a68c3ec1f3db25f5ae5476a7757bc8dfae92a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8ce5c00ca3ef91e0d3eb4c6e6d6ec7cffa9574c447fd8d54a8d96e7c1c80e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd741b12a7eaa64357041c2d3f4590c898313a7f8f65cd1577594e6ee03a8c38`  
		Last Modified: Wed, 08 Mar 2023 05:10:27 GMT  
		Size: 27.3 MB (27347481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f23b7ade9f88f91c8d5932a48b721712ed509a607d9a05cdeae4cd06de09e5f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220c61b3ab7b82dd3ff3395f9efe2b63e730c3f24284d1519013cf3cda822f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2561b3b559ec9b25bafa07804afa433803291265f7dd847de711224b0f238237`  
		Last Modified: Wed, 08 Mar 2023 05:10:39 GMT  
		Size: 34.6 MB (34593661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:b351315d950a4da70f19d62f4da5dd7f9a445eb8c8d6851a5b6cdddbdafb13cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad39053efde0c294433cd8f9709c6d69a36e1f0af4ffbf81c3d261caffb615`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:15f635e04e894b7646b4ebca40424ddf244867fc663429ea8b877eca172a7cf1`  
		Last Modified: Wed, 08 Mar 2023 05:10:46 GMT  
		Size: 28.0 MB (28015959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230308`

```console
$ docker pull ubuntu@sha256:67211c14fa74f070d27cc59d69a7fa9aeff8e28ea118ef3babc295a0428a6d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230308` - linux; amd64

```console
$ docker pull ubuntu@sha256:7a57c69fe1e9d5b97c5fe649849e79f2cfc3bf11d10bbd5218b4eb61716aebe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d22c0ceb150ddeb2237c5fa3129c0183f3cc6f5eeb2e7aa4016da3ad02140a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2ab09b027e7f3a0c2e8bb1944ac46de38cebab7145f0bd6effebfe5492c818b6`  
		Last Modified: Wed, 08 Mar 2023 05:10:20 GMT  
		Size: 29.5 MB (29533950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230308` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ad18cfdb19dac67bf0072dacea661a817330e5c955d081f4d09914e743ae5d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf0095935ffb29018664cf219d8c1b2c890e3e3c4af89113df23e7330397187`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aea1895b7fd03ef3bc263eef4b6f1dd219fc3286f3ff79495aadb81a88650723`  
		Last Modified: Wed, 08 Mar 2023 05:10:33 GMT  
		Size: 26.1 MB (26140319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230308` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:537da24818633b45fcb65e5285a68c3ec1f3db25f5ae5476a7757bc8dfae92a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8ce5c00ca3ef91e0d3eb4c6e6d6ec7cffa9574c447fd8d54a8d96e7c1c80e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd741b12a7eaa64357041c2d3f4590c898313a7f8f65cd1577594e6ee03a8c38`  
		Last Modified: Wed, 08 Mar 2023 05:10:27 GMT  
		Size: 27.3 MB (27347481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230308` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f23b7ade9f88f91c8d5932a48b721712ed509a607d9a05cdeae4cd06de09e5f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220c61b3ab7b82dd3ff3395f9efe2b63e730c3f24284d1519013cf3cda822f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2561b3b559ec9b25bafa07804afa433803291265f7dd847de711224b0f238237`  
		Last Modified: Wed, 08 Mar 2023 05:10:39 GMT  
		Size: 34.6 MB (34593661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230308` - linux; s390x

```console
$ docker pull ubuntu@sha256:b351315d950a4da70f19d62f4da5dd7f9a445eb8c8d6851a5b6cdddbdafb13cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad39053efde0c294433cd8f9709c6d69a36e1f0af4ffbf81c3d261caffb615`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:15f635e04e894b7646b4ebca40424ddf244867fc663429ea8b877eca172a7cf1`  
		Last Modified: Wed, 08 Mar 2023 05:10:46 GMT  
		Size: 28.0 MB (28015959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:4a6ce3cbf8ca08ffec2e69ec71a0635664d2911a2d5985f9e44d2a264e756706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e37c01607a81ee7737f164af67cb5f5f8e1ecbf82c4f5cfe940675b8e8830ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bcbf2021edfcf5671a4872ded2d62d36cd3a86813acc7bc2471fefce3c2ac2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:55:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:55:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:55:49 GMT
ADD file:827330b6c59e67c5d2edd3ceb3492b97865b15f9246f14710f478d12e94d2048 in / 
# Wed, 08 Mar 2023 05:55:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c09adf37dd1d92aeedd2906b2635d9b7f1eca9f39f51d52f919d26d113c8d35`  
		Last Modified: Wed, 08 Mar 2023 06:38:49 GMT  
		Size: 25.1 MB (25067205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a79f91eb2bb4ffc5d96c58a06fda63550bf94a1a6b2e9ef2f835e52ca8a04ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25760037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c48db988d0f48de4461bb2bf49524880c28c5863b1ba5b175a9d7c284b009`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:57:57 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:57:58 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:57:59 GMT
ADD file:884e00dc91bf6d392fa3d117913cc2534177128322d89137bfb8b2734bc38579 in / 
# Wed, 08 Mar 2023 05:58:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f720bb411d1d3a6b6c043988c66cdaeee655f968c6eabf7f1ada7ac1529b046`  
		Last Modified: Wed, 08 Mar 2023 06:38:43 GMT  
		Size: 25.8 MB (25760037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:c69324f895a9152b8a80f9d310710a9d2ef987330d04bc20dbfe23e79e5183bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997349fe1813d9306e1ad38084ecc78950e221fe4f75cd9a85e5213139fcd80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 06:11:04 GMT
ARG RELEASE
# Wed, 08 Mar 2023 06:11:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 06:11:06 GMT
ADD file:974d67ca1d5bcaacbc707820609d36af0d7ed3ff7179a702a4aa56dcc43f79f3 in / 
# Wed, 08 Mar 2023 06:11:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e7f1a81217015da9b8db635ad002e08952988dc4100cbec474290e8524391920`  
		Last Modified: Wed, 08 Mar 2023 06:39:01 GMT  
		Size: 25.5 MB (25488878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230412`

```console
$ docker pull ubuntu@sha256:fa3d554880b4d7a8a58a54725760ae493ad6ebf1fb26cb8a8e0ce8c6b314878f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `ubuntu:kinetic-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:67211c14fa74f070d27cc59d69a7fa9aeff8e28ea118ef3babc295a0428a6d21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:7a57c69fe1e9d5b97c5fe649849e79f2cfc3bf11d10bbd5218b4eb61716aebe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d22c0ceb150ddeb2237c5fa3129c0183f3cc6f5eeb2e7aa4016da3ad02140a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2ab09b027e7f3a0c2e8bb1944ac46de38cebab7145f0bd6effebfe5492c818b6`  
		Last Modified: Wed, 08 Mar 2023 05:10:20 GMT  
		Size: 29.5 MB (29533950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ad18cfdb19dac67bf0072dacea661a817330e5c955d081f4d09914e743ae5d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf0095935ffb29018664cf219d8c1b2c890e3e3c4af89113df23e7330397187`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aea1895b7fd03ef3bc263eef4b6f1dd219fc3286f3ff79495aadb81a88650723`  
		Last Modified: Wed, 08 Mar 2023 05:10:33 GMT  
		Size: 26.1 MB (26140319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:537da24818633b45fcb65e5285a68c3ec1f3db25f5ae5476a7757bc8dfae92a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8ce5c00ca3ef91e0d3eb4c6e6d6ec7cffa9574c447fd8d54a8d96e7c1c80e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cd741b12a7eaa64357041c2d3f4590c898313a7f8f65cd1577594e6ee03a8c38`  
		Last Modified: Wed, 08 Mar 2023 05:10:27 GMT  
		Size: 27.3 MB (27347481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f23b7ade9f88f91c8d5932a48b721712ed509a607d9a05cdeae4cd06de09e5f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220c61b3ab7b82dd3ff3395f9efe2b63e730c3f24284d1519013cf3cda822f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2561b3b559ec9b25bafa07804afa433803291265f7dd847de711224b0f238237`  
		Last Modified: Wed, 08 Mar 2023 05:10:39 GMT  
		Size: 34.6 MB (34593661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:b351315d950a4da70f19d62f4da5dd7f9a445eb8c8d6851a5b6cdddbdafb13cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad39053efde0c294433cd8f9709c6d69a36e1f0af4ffbf81c3d261caffb615`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:15f635e04e894b7646b4ebca40424ddf244867fc663429ea8b877eca172a7cf1`  
		Last Modified: Wed, 08 Mar 2023 05:10:46 GMT  
		Size: 28.0 MB (28015959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:87cb4adffc1badb17b483120780cafc4ae0c7558e463a604c911dd38762f8483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f18a21d414ad3c0a8eea08fec8f98d730c5c02ddb0d5fef9c60ca72ac53329c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c92df8590c370b0dcf10c9273b5c18a74e08fb6089ae37d4ad9590fbdecc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cdca6f9f82cb2f31168afd36307721605cb5f89b51b97fa630583843ddb624a4`  
		Last Modified: Sat, 15 Apr 2023 05:20:43 GMT  
		Size: 26.8 MB (26825187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e685540e6030c9b728fa6485ca8e844d824e064c9a790bc54e6e6507974ba42e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24559160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e4ad84aaa1e06e217b7ed880b9bea183f12a02bb5b8408f57855354fbd91c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 18:18:28 GMT
ARG RELEASE
# Tue, 14 Mar 2023 18:18:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 18:18:30 GMT
ADD file:dc39df38ee577fc1ddb753815787f9a90231d34a28c65e14298d136132c8d7d5 in / 
# Tue, 14 Mar 2023 18:18:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec8b1962079f6d8d8477e2e227966fcf2e91d26a81735eb5f0411f84cbf8740`  
		Last Modified: Tue, 14 Mar 2023 18:47:12 GMT  
		Size: 24.6 MB (24559160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b864a1f0e9f2686fcaa86491f78d38af1b9e8e53e965df39d991a8b685bf7c74
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26007489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e399e758a4b24fbecd3eed7dbaadf0eb3aa45f2ee4b2c133561693f31008b42b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:38:32 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:38:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:38:40 GMT
ADD file:2562122b72f2bcdd0678a1bd0836dcbf376a8e33078452497d85ed0cd425391f in / 
# Tue, 14 Mar 2023 17:38:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff6383e8c55f097496fc03e31f40ad77007ac50d51f9735a1d45789985087387`  
		Last Modified: Tue, 14 Mar 2023 18:47:06 GMT  
		Size: 26.0 MB (26007489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:1840997cef13af4d355cf1b5bda18e68073cc6aefe673bd36cb93ea91f3452a2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25634517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6744e3a8d8d30ea66143d1d2ba080a6cb9a9e1356857de142edfd33ddefb5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:47:18 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:47:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:47:20 GMT
ADD file:1ed4a1aa279c8c4fd49f73ed214f53835caecef222778b80716ba71fe60cc7f0 in / 
# Tue, 14 Mar 2023 17:47:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de8d2f62d0190fb3786c431d236f8d6178a12304755c3c13b8c1ff4d6097587f`  
		Last Modified: Tue, 14 Mar 2023 18:47:26 GMT  
		Size: 25.6 MB (25634517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230415`

```console
$ docker pull ubuntu@sha256:5fc95db3ff6c6e0f531c6e5f5175263b2d263a879cc2a6d01aa172fb8d75c8e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `ubuntu:lunar-20230415` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f18a21d414ad3c0a8eea08fec8f98d730c5c02ddb0d5fef9c60ca72ac53329c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c92df8590c370b0dcf10c9273b5c18a74e08fb6089ae37d4ad9590fbdecc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cdca6f9f82cb2f31168afd36307721605cb5f89b51b97fa630583843ddb624a4`  
		Last Modified: Sat, 15 Apr 2023 05:20:43 GMT  
		Size: 26.8 MB (26825187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230415` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:4a6ce3cbf8ca08ffec2e69ec71a0635664d2911a2d5985f9e44d2a264e756706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e37c01607a81ee7737f164af67cb5f5f8e1ecbf82c4f5cfe940675b8e8830ee1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bcbf2021edfcf5671a4872ded2d62d36cd3a86813acc7bc2471fefce3c2ac2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:55:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:55:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:55:43 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:55:49 GMT
ADD file:827330b6c59e67c5d2edd3ceb3492b97865b15f9246f14710f478d12e94d2048 in / 
# Wed, 08 Mar 2023 05:55:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c09adf37dd1d92aeedd2906b2635d9b7f1eca9f39f51d52f919d26d113c8d35`  
		Last Modified: Wed, 08 Mar 2023 06:38:49 GMT  
		Size: 25.1 MB (25067205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a79f91eb2bb4ffc5d96c58a06fda63550bf94a1a6b2e9ef2f835e52ca8a04ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25760037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c48db988d0f48de4461bb2bf49524880c28c5863b1ba5b175a9d7c284b009`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 05:57:57 GMT
ARG RELEASE
# Wed, 08 Mar 2023 05:57:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 05:57:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 05:57:58 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 05:57:59 GMT
ADD file:884e00dc91bf6d392fa3d117913cc2534177128322d89137bfb8b2734bc38579 in / 
# Wed, 08 Mar 2023 05:58:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f720bb411d1d3a6b6c043988c66cdaeee655f968c6eabf7f1ada7ac1529b046`  
		Last Modified: Wed, 08 Mar 2023 06:38:43 GMT  
		Size: 25.8 MB (25760037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:c69324f895a9152b8a80f9d310710a9d2ef987330d04bc20dbfe23e79e5183bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997349fe1813d9306e1ad38084ecc78950e221fe4f75cd9a85e5213139fcd80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 06:11:04 GMT
ARG RELEASE
# Wed, 08 Mar 2023 06:11:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 06:11:04 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 08 Mar 2023 06:11:06 GMT
ADD file:974d67ca1d5bcaacbc707820609d36af0d7ed3ff7179a702a4aa56dcc43f79f3 in / 
# Wed, 08 Mar 2023 06:11:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e7f1a81217015da9b8db635ad002e08952988dc4100cbec474290e8524391920`  
		Last Modified: Wed, 08 Mar 2023 06:39:01 GMT  
		Size: 25.5 MB (25488878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
