<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20231211`](#ubuntufocal-20231211)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20231211.1`](#ubuntujammy-202312111)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20231128`](#ubuntulunar-20231128)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20231128`](#ubuntumantic-20231128)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20231221`](#ubuntunoble-20231221)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:f2034e7195f61334e6caff6ecf2e965f92d11e888309065da85ff50c617732b8
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
$ docker pull ubuntu@sha256:bac6081102aae54ba4bcc714695b8f637e42768c7f376f374c428bab043ddc0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27512774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78909c2b360d866b3220655c0b079838258b8891a12ac25fc670f0cbb54229f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2e23f3094773c2f173890f9fd1f4b562dda2d937064b88d37a190019ea46f340
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92cb36a53cbf15e52d3302b465adb134bf5694cc2d10a0721bd224bd6cef53f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:327025e411b20fc483e604bf05660a6c64a00f43d1c60ba3131b556b18a07511`  
		Last Modified: Wed, 13 Dec 2023 10:49:11 GMT  
		Size: 23.6 MB (23622456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:080169816683e6f063d3903434565624287828ecfd06bd2f813b30325e8b1eca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde9c12d7d3f936f56d545cc36391de434bbe311fd9d60f98e496c527cf58f21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c083ada488db06e4b75cf31d279946b478acfa048e2f0aca39f8ef90c2006386
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32075270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1aa8372f4210a7209e1250808d562df02be12280f883289c22fcf4e62d154`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d20838a29743bf51a2def4bf0d3bc0cb24f5287a64cbd5d90d451bca5da0626a`  
		Last Modified: Wed, 13 Dec 2023 10:49:17 GMT  
		Size: 32.1 MB (32075270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:f426bc1a32578d1f95602b024cab9c6e2def3ba6538194e8847d0af78bcb41c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7828dd4376eb5359717c5f176d47e83276c0b508ba722a7a0c2da250a9847ba9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26a2c360f5949b32e39caa299bdd3a19ebd600431e71b605885f64f7be0d1862`  
		Last Modified: Wed, 13 Dec 2023 10:49:23 GMT  
		Size: 26.4 MB (26363864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:6042500cf4b44023ea1894effe7890666b0c5c7871ed83a97c36c76ae560bb9b
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
$ docker pull ubuntu@sha256:bbf3d1baa208b7649d1d0264ef7d522e1dc0deeeaaf6085bf8e4618867f03494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29547485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174c8c134b2a94b5bb0b37d9a2b6ba0663d82d23ebf62bd51f74a2fd457333da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6bd78eb69d21a2266b96a851002324b769483d704df3b73a37f78e6fe767f04
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26635272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb4f0da36a059c0aa61899290aec075393d2865c1edea112ea81ceaa12d53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d33cdf8c116214cd1f23278abc2741878af19658bf65c210a48280807622d871`  
		Last Modified: Tue, 12 Dec 2023 11:55:37 GMT  
		Size: 26.6 MB (26635272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ba545858745d6307f0d1064d0d25365466f78d02f866cf4efb9e1326a4c196ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da935f0649133cbea2f5ad83db14bf782aa5ee9ad17cd609253e3750201a9298`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1021a5203fe161639721ebfb11d2523c891c3092dd6c239f54995b554cbdc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34521615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce679385b55913348f173b0d7a11c79a06f61abc95525b7e51f2705dd327fa5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:a325aa8b607ceefbf215a70887e7bce9c4413e510692087b7cd1be6db8e5191d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28027192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446a5eabbfe22b430a73fb05c818982ff8013141f79a000474d5e0e7e751b52e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:5a828e28de105c3d7821c4442f0f5d1c52dc16acf4999d5f31a3bc0f03f06edd
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
$ docker pull ubuntu@sha256:ea1285dffce8a938ef356908d1be741da594310c8dced79b870d66808cb12b0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26886018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cdeba72b994748f5eb1f525a70a9cc553b66037ec37e23645fbf3f0f5c160d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6360b371721185fefbbad6763ab745900f1b2f7714570234473232dd575fc07f`  
		Last Modified: Tue, 28 Nov 2023 09:27:24 GMT  
		Size: 26.9 MB (26886018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:27ec9bb1046f930093435520691bff3f4e3c871b55dc5293c474281846951c66
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f2ae218c0330ff4ca6c8a11e60f2993488ff3fe6285e7df42d555d1910eb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2643114b278119e4a1e5025ec57ada8a2b3ef31628c7417686d0a688c640fb6d`  
		Last Modified: Tue, 28 Nov 2023 09:27:37 GMT  
		Size: 24.6 MB (24640780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15db3e6b59a9119916cd858d52e6d4cef718c02c781dce5cf0fe5d03d933b73c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c28bcdb9f7216366ebe5113f796f5404a28dea1790f34929e1251264e45a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8df4a5e885db4891759c9d9cfc2e43aee3f9aabf9527d938bb46d115e03e8da`  
		Last Modified: Tue, 28 Nov 2023 09:27:30 GMT  
		Size: 26.1 MB (26079900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c28fa7ea101bb0a00eff5a308adc23ab2e38233fb5d774159312e3c3a76c8117
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30917966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e62d935d40f82192cbff6f4484a55808f2768c86a03a58d529a523394d24c12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:560944132ff1df4504e996c465ce940bd939a402ada0807793d05ca35535070c`  
		Last Modified: Tue, 28 Nov 2023 09:27:55 GMT  
		Size: 30.9 MB (30917966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:b9e4e416dbed67b9ddc739e89ef6352e80636153335eda2083a5f8e2895b1a27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25705524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffbdfac8172ad59a8598c19128ed08f06dfd85348b13a614aa85ff9d67a093`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1590276a0ea31f1d9c79822d84f64652790d6ba51de9ecdee58adc2e3a6ecdd`  
		Last Modified: Tue, 28 Nov 2023 09:28:01 GMT  
		Size: 25.7 MB (25705524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:cbc171ba52575fec0601f01abf6fdec67f8ed227658cacbc10d778ac3b218307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:8d093e0651575a6437cc4a3d561f892a345d263aeac6156ef378fe6a4ccabd4c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27273553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483a94112583ff9c6d0a7b67348fc3b0ee5bbf104a86a9e24585c9ad1028fd25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:767829bcf202e4fa7e777f29d390307e29ac437f131685a1ff1293d44705ca23`  
		Last Modified: Thu, 30 Nov 2023 18:06:39 GMT  
		Size: 27.3 MB (27273553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f5ac92fb1f602adf15449871e0593a7b38f7a461de589810bd887e49928ee62d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25203103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c99846a5ef249a3f390310f0283176cee9c661d1221d866b942b11f50ed31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:081b2ed8534a247171d83183d75e8113b3237c45f1b12933b7d6833e80a58198`  
		Last Modified: Thu, 30 Nov 2023 18:06:52 GMT  
		Size: 25.2 MB (25203103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:694c2aa053066101c5f29e909d4baaea478ac50e499d452f510c10e961ebb42f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26391312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382e20053971e462c74b86d6dd56f440693ddf596f0fb4989a9ef87ffb1bd5a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b227d7805fb6cba5d091f0565054ae9ed1e13a6e2df91de4cfb41f70e208da31`  
		Last Modified: Thu, 30 Nov 2023 18:06:46 GMT  
		Size: 26.4 MB (26391312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:22c4449e6ef2d40adecaf8ecc4df1bd80a701c12f89f29f15245189cd3da22b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31346558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eab81e5b01a3726fd0cdbe70cf8d42317086e71ef61ad68667b29af27db455b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86fa66fe8d0305c6369ae9bf03d1677c1d99b5cefbef6dd550617a300956d5b6`  
		Last Modified: Thu, 30 Nov 2023 18:06:59 GMT  
		Size: 31.3 MB (31346558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:f9bd1296086163c80f76427fb987a4ecf6799b490c724fc0bea92e66d60620cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bd2cee374af30258d9d818b2ef084ef72674c8a1304bc94b177dc70da33166`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5ab01e9ae41fd34fc412118be6d5e21f82290394cf86ba09cd54207fa341e2d9`  
		Last Modified: Thu, 30 Nov 2023 18:07:13 GMT  
		Size: 27.1 MB (27094013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:38d380071057443ebb6d65566c03a98eaec411e84e04e5e16cff49b1d6fdc9a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:145bacc9db29ff9c9c021284e5b7b22f1193fc38556c578250c926cf3c883a13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29469158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1d0ba034dc2bf324fbbd0096382576e6f4a407881bd22300b0013ce8626cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ce3d5b1e4efe5d8f8dd38f54962ab6cb52eeacff317c7388d838d3f6f6fef468`  
		Last Modified: Thu, 21 Dec 2023 09:36:03 GMT  
		Size: 29.5 MB (29469158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a8f13cbf5af7cf43d01fb67fbdf46f1fa32f8bfd9c886ad7884f801a6cda480c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24968813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb46bc632edaae61f9d26aa64e3c39e01812d81a1fc1b579383b728ab8b6e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb8e9622ad1d4dae8ae54e1405f2b2a234d32bd778d99df806fe4523a6e2552d`  
		Last Modified: Thu, 21 Dec 2023 09:36:16 GMT  
		Size: 25.0 MB (24968813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70763dc887b503de95fde4a4304e9d954780ae5a33798c88185054a05c4f3d7b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26466767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f998bc3cd169ccb274afc7238a50a61791493ad78b5cb791a2367a7a824452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0bc38803e76501f9a808531dd4b0e0d44d0840af31dda276f6feb185920548be`  
		Last Modified: Thu, 21 Dec 2023 09:36:09 GMT  
		Size: 26.5 MB (26466767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0824d39c30d7b86b0d468eb67500b6e863bafdca015f15dbcf5aedd3c33c4517
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31412378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445321c04f5dd0e5aea3e0c8d6ab2d1cf83713d967d98174b0073bcb77de52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6960966bb8160819f898baca4c8afea9efc64b74c051eeeb081f145b80ce6873`  
		Last Modified: Thu, 21 Dec 2023 09:36:22 GMT  
		Size: 31.4 MB (31412378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:5a4044a6506755b6b63d516ffc7a63b65cf5f4e2a6993a6279b4e02338ace2fe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45061dbc3dd151de103b8f8158bf0d3010034accf18af7e19346eaf1a49ebcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0959e1da813204db7d13dafafebed7582197d5b796af1bb2379cd2981bba233f`  
		Last Modified: Thu, 21 Dec 2023 09:36:28 GMT  
		Size: 27.6 MB (27610529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:38d380071057443ebb6d65566c03a98eaec411e84e04e5e16cff49b1d6fdc9a0
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
$ docker pull ubuntu@sha256:145bacc9db29ff9c9c021284e5b7b22f1193fc38556c578250c926cf3c883a13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29469158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1d0ba034dc2bf324fbbd0096382576e6f4a407881bd22300b0013ce8626cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ce3d5b1e4efe5d8f8dd38f54962ab6cb52eeacff317c7388d838d3f6f6fef468`  
		Last Modified: Thu, 21 Dec 2023 09:36:03 GMT  
		Size: 29.5 MB (29469158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a8f13cbf5af7cf43d01fb67fbdf46f1fa32f8bfd9c886ad7884f801a6cda480c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24968813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb46bc632edaae61f9d26aa64e3c39e01812d81a1fc1b579383b728ab8b6e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb8e9622ad1d4dae8ae54e1405f2b2a234d32bd778d99df806fe4523a6e2552d`  
		Last Modified: Thu, 21 Dec 2023 09:36:16 GMT  
		Size: 25.0 MB (24968813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70763dc887b503de95fde4a4304e9d954780ae5a33798c88185054a05c4f3d7b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26466767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f998bc3cd169ccb274afc7238a50a61791493ad78b5cb791a2367a7a824452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0bc38803e76501f9a808531dd4b0e0d44d0840af31dda276f6feb185920548be`  
		Last Modified: Thu, 21 Dec 2023 09:36:09 GMT  
		Size: 26.5 MB (26466767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0824d39c30d7b86b0d468eb67500b6e863bafdca015f15dbcf5aedd3c33c4517
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31412378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445321c04f5dd0e5aea3e0c8d6ab2d1cf83713d967d98174b0073bcb77de52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6960966bb8160819f898baca4c8afea9efc64b74c051eeeb081f145b80ce6873`  
		Last Modified: Thu, 21 Dec 2023 09:36:22 GMT  
		Size: 31.4 MB (31412378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:5a4044a6506755b6b63d516ffc7a63b65cf5f4e2a6993a6279b4e02338ace2fe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45061dbc3dd151de103b8f8158bf0d3010034accf18af7e19346eaf1a49ebcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0959e1da813204db7d13dafafebed7582197d5b796af1bb2379cd2981bba233f`  
		Last Modified: Thu, 21 Dec 2023 09:36:28 GMT  
		Size: 27.6 MB (27610529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:f2034e7195f61334e6caff6ecf2e965f92d11e888309065da85ff50c617732b8
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
$ docker pull ubuntu@sha256:bac6081102aae54ba4bcc714695b8f637e42768c7f376f374c428bab043ddc0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27512774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78909c2b360d866b3220655c0b079838258b8891a12ac25fc670f0cbb54229f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2e23f3094773c2f173890f9fd1f4b562dda2d937064b88d37a190019ea46f340
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92cb36a53cbf15e52d3302b465adb134bf5694cc2d10a0721bd224bd6cef53f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:327025e411b20fc483e604bf05660a6c64a00f43d1c60ba3131b556b18a07511`  
		Last Modified: Wed, 13 Dec 2023 10:49:11 GMT  
		Size: 23.6 MB (23622456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:080169816683e6f063d3903434565624287828ecfd06bd2f813b30325e8b1eca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde9c12d7d3f936f56d545cc36391de434bbe311fd9d60f98e496c527cf58f21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c083ada488db06e4b75cf31d279946b478acfa048e2f0aca39f8ef90c2006386
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32075270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1aa8372f4210a7209e1250808d562df02be12280f883289c22fcf4e62d154`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d20838a29743bf51a2def4bf0d3bc0cb24f5287a64cbd5d90d451bca5da0626a`  
		Last Modified: Wed, 13 Dec 2023 10:49:17 GMT  
		Size: 32.1 MB (32075270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:f426bc1a32578d1f95602b024cab9c6e2def3ba6538194e8847d0af78bcb41c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7828dd4376eb5359717c5f176d47e83276c0b508ba722a7a0c2da250a9847ba9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26a2c360f5949b32e39caa299bdd3a19ebd600431e71b605885f64f7be0d1862`  
		Last Modified: Wed, 13 Dec 2023 10:49:23 GMT  
		Size: 26.4 MB (26363864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20231211`

```console
$ docker pull ubuntu@sha256:f2034e7195f61334e6caff6ecf2e965f92d11e888309065da85ff50c617732b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20231211` - linux; amd64

```console
$ docker pull ubuntu@sha256:bac6081102aae54ba4bcc714695b8f637e42768c7f376f374c428bab043ddc0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27512774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78909c2b360d866b3220655c0b079838258b8891a12ac25fc670f0cbb54229f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231211` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2e23f3094773c2f173890f9fd1f4b562dda2d937064b88d37a190019ea46f340
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92cb36a53cbf15e52d3302b465adb134bf5694cc2d10a0721bd224bd6cef53f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:327025e411b20fc483e604bf05660a6c64a00f43d1c60ba3131b556b18a07511`  
		Last Modified: Wed, 13 Dec 2023 10:49:11 GMT  
		Size: 23.6 MB (23622456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231211` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:080169816683e6f063d3903434565624287828ecfd06bd2f813b30325e8b1eca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde9c12d7d3f936f56d545cc36391de434bbe311fd9d60f98e496c527cf58f21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231211` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c083ada488db06e4b75cf31d279946b478acfa048e2f0aca39f8ef90c2006386
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32075270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1aa8372f4210a7209e1250808d562df02be12280f883289c22fcf4e62d154`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d20838a29743bf51a2def4bf0d3bc0cb24f5287a64cbd5d90d451bca5da0626a`  
		Last Modified: Wed, 13 Dec 2023 10:49:17 GMT  
		Size: 32.1 MB (32075270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231211` - linux; s390x

```console
$ docker pull ubuntu@sha256:f426bc1a32578d1f95602b024cab9c6e2def3ba6538194e8847d0af78bcb41c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7828dd4376eb5359717c5f176d47e83276c0b508ba722a7a0c2da250a9847ba9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26a2c360f5949b32e39caa299bdd3a19ebd600431e71b605885f64f7be0d1862`  
		Last Modified: Wed, 13 Dec 2023 10:49:23 GMT  
		Size: 26.4 MB (26363864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:6042500cf4b44023ea1894effe7890666b0c5c7871ed83a97c36c76ae560bb9b
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
$ docker pull ubuntu@sha256:bbf3d1baa208b7649d1d0264ef7d522e1dc0deeeaaf6085bf8e4618867f03494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29547485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174c8c134b2a94b5bb0b37d9a2b6ba0663d82d23ebf62bd51f74a2fd457333da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6bd78eb69d21a2266b96a851002324b769483d704df3b73a37f78e6fe767f04
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26635272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb4f0da36a059c0aa61899290aec075393d2865c1edea112ea81ceaa12d53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d33cdf8c116214cd1f23278abc2741878af19658bf65c210a48280807622d871`  
		Last Modified: Tue, 12 Dec 2023 11:55:37 GMT  
		Size: 26.6 MB (26635272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ba545858745d6307f0d1064d0d25365466f78d02f866cf4efb9e1326a4c196ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da935f0649133cbea2f5ad83db14bf782aa5ee9ad17cd609253e3750201a9298`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1021a5203fe161639721ebfb11d2523c891c3092dd6c239f54995b554cbdc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34521615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce679385b55913348f173b0d7a11c79a06f61abc95525b7e51f2705dd327fa5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:a325aa8b607ceefbf215a70887e7bce9c4413e510692087b7cd1be6db8e5191d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28027192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446a5eabbfe22b430a73fb05c818982ff8013141f79a000474d5e0e7e751b52e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20231211.1`

```console
$ docker pull ubuntu@sha256:6042500cf4b44023ea1894effe7890666b0c5c7871ed83a97c36c76ae560bb9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20231211.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:bbf3d1baa208b7649d1d0264ef7d522e1dc0deeeaaf6085bf8e4618867f03494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29547485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174c8c134b2a94b5bb0b37d9a2b6ba0663d82d23ebf62bd51f74a2fd457333da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231211.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6bd78eb69d21a2266b96a851002324b769483d704df3b73a37f78e6fe767f04
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26635272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb4f0da36a059c0aa61899290aec075393d2865c1edea112ea81ceaa12d53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d33cdf8c116214cd1f23278abc2741878af19658bf65c210a48280807622d871`  
		Last Modified: Tue, 12 Dec 2023 11:55:37 GMT  
		Size: 26.6 MB (26635272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231211.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ba545858745d6307f0d1064d0d25365466f78d02f866cf4efb9e1326a4c196ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da935f0649133cbea2f5ad83db14bf782aa5ee9ad17cd609253e3750201a9298`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231211.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1021a5203fe161639721ebfb11d2523c891c3092dd6c239f54995b554cbdc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34521615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce679385b55913348f173b0d7a11c79a06f61abc95525b7e51f2705dd327fa5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231211.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:a325aa8b607ceefbf215a70887e7bce9c4413e510692087b7cd1be6db8e5191d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28027192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446a5eabbfe22b430a73fb05c818982ff8013141f79a000474d5e0e7e751b52e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:6042500cf4b44023ea1894effe7890666b0c5c7871ed83a97c36c76ae560bb9b
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
$ docker pull ubuntu@sha256:bbf3d1baa208b7649d1d0264ef7d522e1dc0deeeaaf6085bf8e4618867f03494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29547485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174c8c134b2a94b5bb0b37d9a2b6ba0663d82d23ebf62bd51f74a2fd457333da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6bd78eb69d21a2266b96a851002324b769483d704df3b73a37f78e6fe767f04
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26635272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb4f0da36a059c0aa61899290aec075393d2865c1edea112ea81ceaa12d53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d33cdf8c116214cd1f23278abc2741878af19658bf65c210a48280807622d871`  
		Last Modified: Tue, 12 Dec 2023 11:55:37 GMT  
		Size: 26.6 MB (26635272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ba545858745d6307f0d1064d0d25365466f78d02f866cf4efb9e1326a4c196ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da935f0649133cbea2f5ad83db14bf782aa5ee9ad17cd609253e3750201a9298`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1021a5203fe161639721ebfb11d2523c891c3092dd6c239f54995b554cbdc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34521615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce679385b55913348f173b0d7a11c79a06f61abc95525b7e51f2705dd327fa5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6d5f22cb7a5ae76d71ff8d8d5254febad219eb4adbf9b849b5e1d5bd967691cd`  
		Last Modified: Tue, 12 Dec 2023 11:55:44 GMT  
		Size: 34.5 MB (34521615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:a325aa8b607ceefbf215a70887e7bce9c4413e510692087b7cd1be6db8e5191d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28027192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446a5eabbfe22b430a73fb05c818982ff8013141f79a000474d5e0e7e751b52e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:5a828e28de105c3d7821c4442f0f5d1c52dc16acf4999d5f31a3bc0f03f06edd
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
$ docker pull ubuntu@sha256:ea1285dffce8a938ef356908d1be741da594310c8dced79b870d66808cb12b0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26886018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cdeba72b994748f5eb1f525a70a9cc553b66037ec37e23645fbf3f0f5c160d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6360b371721185fefbbad6763ab745900f1b2f7714570234473232dd575fc07f`  
		Last Modified: Tue, 28 Nov 2023 09:27:24 GMT  
		Size: 26.9 MB (26886018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:27ec9bb1046f930093435520691bff3f4e3c871b55dc5293c474281846951c66
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f2ae218c0330ff4ca6c8a11e60f2993488ff3fe6285e7df42d555d1910eb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2643114b278119e4a1e5025ec57ada8a2b3ef31628c7417686d0a688c640fb6d`  
		Last Modified: Tue, 28 Nov 2023 09:27:37 GMT  
		Size: 24.6 MB (24640780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15db3e6b59a9119916cd858d52e6d4cef718c02c781dce5cf0fe5d03d933b73c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c28bcdb9f7216366ebe5113f796f5404a28dea1790f34929e1251264e45a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8df4a5e885db4891759c9d9cfc2e43aee3f9aabf9527d938bb46d115e03e8da`  
		Last Modified: Tue, 28 Nov 2023 09:27:30 GMT  
		Size: 26.1 MB (26079900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c28fa7ea101bb0a00eff5a308adc23ab2e38233fb5d774159312e3c3a76c8117
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30917966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e62d935d40f82192cbff6f4484a55808f2768c86a03a58d529a523394d24c12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:560944132ff1df4504e996c465ce940bd939a402ada0807793d05ca35535070c`  
		Last Modified: Tue, 28 Nov 2023 09:27:55 GMT  
		Size: 30.9 MB (30917966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:b9e4e416dbed67b9ddc739e89ef6352e80636153335eda2083a5f8e2895b1a27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25705524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffbdfac8172ad59a8598c19128ed08f06dfd85348b13a614aa85ff9d67a093`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1590276a0ea31f1d9c79822d84f64652790d6ba51de9ecdee58adc2e3a6ecdd`  
		Last Modified: Tue, 28 Nov 2023 09:28:01 GMT  
		Size: 25.7 MB (25705524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20231128`

```console
$ docker pull ubuntu@sha256:5a828e28de105c3d7821c4442f0f5d1c52dc16acf4999d5f31a3bc0f03f06edd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20231128` - linux; amd64

```console
$ docker pull ubuntu@sha256:ea1285dffce8a938ef356908d1be741da594310c8dced79b870d66808cb12b0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26886018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cdeba72b994748f5eb1f525a70a9cc553b66037ec37e23645fbf3f0f5c160d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6360b371721185fefbbad6763ab745900f1b2f7714570234473232dd575fc07f`  
		Last Modified: Tue, 28 Nov 2023 09:27:24 GMT  
		Size: 26.9 MB (26886018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231128` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:27ec9bb1046f930093435520691bff3f4e3c871b55dc5293c474281846951c66
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f2ae218c0330ff4ca6c8a11e60f2993488ff3fe6285e7df42d555d1910eb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2643114b278119e4a1e5025ec57ada8a2b3ef31628c7417686d0a688c640fb6d`  
		Last Modified: Tue, 28 Nov 2023 09:27:37 GMT  
		Size: 24.6 MB (24640780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231128` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15db3e6b59a9119916cd858d52e6d4cef718c02c781dce5cf0fe5d03d933b73c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c28bcdb9f7216366ebe5113f796f5404a28dea1790f34929e1251264e45a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8df4a5e885db4891759c9d9cfc2e43aee3f9aabf9527d938bb46d115e03e8da`  
		Last Modified: Tue, 28 Nov 2023 09:27:30 GMT  
		Size: 26.1 MB (26079900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231128` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c28fa7ea101bb0a00eff5a308adc23ab2e38233fb5d774159312e3c3a76c8117
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30917966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e62d935d40f82192cbff6f4484a55808f2768c86a03a58d529a523394d24c12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:560944132ff1df4504e996c465ce940bd939a402ada0807793d05ca35535070c`  
		Last Modified: Tue, 28 Nov 2023 09:27:55 GMT  
		Size: 30.9 MB (30917966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231128` - linux; s390x

```console
$ docker pull ubuntu@sha256:b9e4e416dbed67b9ddc739e89ef6352e80636153335eda2083a5f8e2895b1a27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25705524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffbdfac8172ad59a8598c19128ed08f06dfd85348b13a614aa85ff9d67a093`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1590276a0ea31f1d9c79822d84f64652790d6ba51de9ecdee58adc2e3a6ecdd`  
		Last Modified: Tue, 28 Nov 2023 09:28:01 GMT  
		Size: 25.7 MB (25705524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:cbc171ba52575fec0601f01abf6fdec67f8ed227658cacbc10d778ac3b218307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:8d093e0651575a6437cc4a3d561f892a345d263aeac6156ef378fe6a4ccabd4c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27273553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483a94112583ff9c6d0a7b67348fc3b0ee5bbf104a86a9e24585c9ad1028fd25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:767829bcf202e4fa7e777f29d390307e29ac437f131685a1ff1293d44705ca23`  
		Last Modified: Thu, 30 Nov 2023 18:06:39 GMT  
		Size: 27.3 MB (27273553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f5ac92fb1f602adf15449871e0593a7b38f7a461de589810bd887e49928ee62d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25203103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c99846a5ef249a3f390310f0283176cee9c661d1221d866b942b11f50ed31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:081b2ed8534a247171d83183d75e8113b3237c45f1b12933b7d6833e80a58198`  
		Last Modified: Thu, 30 Nov 2023 18:06:52 GMT  
		Size: 25.2 MB (25203103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:694c2aa053066101c5f29e909d4baaea478ac50e499d452f510c10e961ebb42f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26391312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382e20053971e462c74b86d6dd56f440693ddf596f0fb4989a9ef87ffb1bd5a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b227d7805fb6cba5d091f0565054ae9ed1e13a6e2df91de4cfb41f70e208da31`  
		Last Modified: Thu, 30 Nov 2023 18:06:46 GMT  
		Size: 26.4 MB (26391312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:22c4449e6ef2d40adecaf8ecc4df1bd80a701c12f89f29f15245189cd3da22b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31346558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eab81e5b01a3726fd0cdbe70cf8d42317086e71ef61ad68667b29af27db455b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86fa66fe8d0305c6369ae9bf03d1677c1d99b5cefbef6dd550617a300956d5b6`  
		Last Modified: Thu, 30 Nov 2023 18:06:59 GMT  
		Size: 31.3 MB (31346558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:f9bd1296086163c80f76427fb987a4ecf6799b490c724fc0bea92e66d60620cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bd2cee374af30258d9d818b2ef084ef72674c8a1304bc94b177dc70da33166`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5ab01e9ae41fd34fc412118be6d5e21f82290394cf86ba09cd54207fa341e2d9`  
		Last Modified: Thu, 30 Nov 2023 18:07:13 GMT  
		Size: 27.1 MB (27094013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20231128`

```console
$ docker pull ubuntu@sha256:cbc171ba52575fec0601f01abf6fdec67f8ed227658cacbc10d778ac3b218307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20231128` - linux; amd64

```console
$ docker pull ubuntu@sha256:8d093e0651575a6437cc4a3d561f892a345d263aeac6156ef378fe6a4ccabd4c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27273553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483a94112583ff9c6d0a7b67348fc3b0ee5bbf104a86a9e24585c9ad1028fd25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:767829bcf202e4fa7e777f29d390307e29ac437f131685a1ff1293d44705ca23`  
		Last Modified: Thu, 30 Nov 2023 18:06:39 GMT  
		Size: 27.3 MB (27273553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231128` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f5ac92fb1f602adf15449871e0593a7b38f7a461de589810bd887e49928ee62d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25203103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c99846a5ef249a3f390310f0283176cee9c661d1221d866b942b11f50ed31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:081b2ed8534a247171d83183d75e8113b3237c45f1b12933b7d6833e80a58198`  
		Last Modified: Thu, 30 Nov 2023 18:06:52 GMT  
		Size: 25.2 MB (25203103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231128` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:694c2aa053066101c5f29e909d4baaea478ac50e499d452f510c10e961ebb42f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26391312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382e20053971e462c74b86d6dd56f440693ddf596f0fb4989a9ef87ffb1bd5a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b227d7805fb6cba5d091f0565054ae9ed1e13a6e2df91de4cfb41f70e208da31`  
		Last Modified: Thu, 30 Nov 2023 18:06:46 GMT  
		Size: 26.4 MB (26391312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231128` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:22c4449e6ef2d40adecaf8ecc4df1bd80a701c12f89f29f15245189cd3da22b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31346558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eab81e5b01a3726fd0cdbe70cf8d42317086e71ef61ad68667b29af27db455b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86fa66fe8d0305c6369ae9bf03d1677c1d99b5cefbef6dd550617a300956d5b6`  
		Last Modified: Thu, 30 Nov 2023 18:06:59 GMT  
		Size: 31.3 MB (31346558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231128` - linux; s390x

```console
$ docker pull ubuntu@sha256:f9bd1296086163c80f76427fb987a4ecf6799b490c724fc0bea92e66d60620cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bd2cee374af30258d9d818b2ef084ef72674c8a1304bc94b177dc70da33166`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5ab01e9ae41fd34fc412118be6d5e21f82290394cf86ba09cd54207fa341e2d9`  
		Last Modified: Thu, 30 Nov 2023 18:07:13 GMT  
		Size: 27.1 MB (27094013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:38d380071057443ebb6d65566c03a98eaec411e84e04e5e16cff49b1d6fdc9a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:145bacc9db29ff9c9c021284e5b7b22f1193fc38556c578250c926cf3c883a13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29469158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1d0ba034dc2bf324fbbd0096382576e6f4a407881bd22300b0013ce8626cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ce3d5b1e4efe5d8f8dd38f54962ab6cb52eeacff317c7388d838d3f6f6fef468`  
		Last Modified: Thu, 21 Dec 2023 09:36:03 GMT  
		Size: 29.5 MB (29469158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a8f13cbf5af7cf43d01fb67fbdf46f1fa32f8bfd9c886ad7884f801a6cda480c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24968813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb46bc632edaae61f9d26aa64e3c39e01812d81a1fc1b579383b728ab8b6e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb8e9622ad1d4dae8ae54e1405f2b2a234d32bd778d99df806fe4523a6e2552d`  
		Last Modified: Thu, 21 Dec 2023 09:36:16 GMT  
		Size: 25.0 MB (24968813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70763dc887b503de95fde4a4304e9d954780ae5a33798c88185054a05c4f3d7b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26466767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f998bc3cd169ccb274afc7238a50a61791493ad78b5cb791a2367a7a824452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0bc38803e76501f9a808531dd4b0e0d44d0840af31dda276f6feb185920548be`  
		Last Modified: Thu, 21 Dec 2023 09:36:09 GMT  
		Size: 26.5 MB (26466767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0824d39c30d7b86b0d468eb67500b6e863bafdca015f15dbcf5aedd3c33c4517
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31412378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445321c04f5dd0e5aea3e0c8d6ab2d1cf83713d967d98174b0073bcb77de52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6960966bb8160819f898baca4c8afea9efc64b74c051eeeb081f145b80ce6873`  
		Last Modified: Thu, 21 Dec 2023 09:36:22 GMT  
		Size: 31.4 MB (31412378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:5a4044a6506755b6b63d516ffc7a63b65cf5f4e2a6993a6279b4e02338ace2fe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45061dbc3dd151de103b8f8158bf0d3010034accf18af7e19346eaf1a49ebcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0959e1da813204db7d13dafafebed7582197d5b796af1bb2379cd2981bba233f`  
		Last Modified: Thu, 21 Dec 2023 09:36:28 GMT  
		Size: 27.6 MB (27610529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20231221`

```console
$ docker pull ubuntu@sha256:38d380071057443ebb6d65566c03a98eaec411e84e04e5e16cff49b1d6fdc9a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20231221` - linux; amd64

```console
$ docker pull ubuntu@sha256:145bacc9db29ff9c9c021284e5b7b22f1193fc38556c578250c926cf3c883a13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29469158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1d0ba034dc2bf324fbbd0096382576e6f4a407881bd22300b0013ce8626cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ce3d5b1e4efe5d8f8dd38f54962ab6cb52eeacff317c7388d838d3f6f6fef468`  
		Last Modified: Thu, 21 Dec 2023 09:36:03 GMT  
		Size: 29.5 MB (29469158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20231221` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:a8f13cbf5af7cf43d01fb67fbdf46f1fa32f8bfd9c886ad7884f801a6cda480c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24968813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb46bc632edaae61f9d26aa64e3c39e01812d81a1fc1b579383b728ab8b6e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb8e9622ad1d4dae8ae54e1405f2b2a234d32bd778d99df806fe4523a6e2552d`  
		Last Modified: Thu, 21 Dec 2023 09:36:16 GMT  
		Size: 25.0 MB (24968813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20231221` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:70763dc887b503de95fde4a4304e9d954780ae5a33798c88185054a05c4f3d7b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26466767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f998bc3cd169ccb274afc7238a50a61791493ad78b5cb791a2367a7a824452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0bc38803e76501f9a808531dd4b0e0d44d0840af31dda276f6feb185920548be`  
		Last Modified: Thu, 21 Dec 2023 09:36:09 GMT  
		Size: 26.5 MB (26466767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20231221` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:0824d39c30d7b86b0d468eb67500b6e863bafdca015f15dbcf5aedd3c33c4517
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31412378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445321c04f5dd0e5aea3e0c8d6ab2d1cf83713d967d98174b0073bcb77de52a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6960966bb8160819f898baca4c8afea9efc64b74c051eeeb081f145b80ce6873`  
		Last Modified: Thu, 21 Dec 2023 09:36:22 GMT  
		Size: 31.4 MB (31412378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20231221` - linux; s390x

```console
$ docker pull ubuntu@sha256:5a4044a6506755b6b63d516ffc7a63b65cf5f4e2a6993a6279b4e02338ace2fe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45061dbc3dd151de103b8f8158bf0d3010034accf18af7e19346eaf1a49ebcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0959e1da813204db7d13dafafebed7582197d5b796af1bb2379cd2981bba233f`  
		Last Modified: Thu, 21 Dec 2023 09:36:28 GMT  
		Size: 27.6 MB (27610529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:cbc171ba52575fec0601f01abf6fdec67f8ed227658cacbc10d778ac3b218307
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
$ docker pull ubuntu@sha256:8d093e0651575a6437cc4a3d561f892a345d263aeac6156ef378fe6a4ccabd4c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27273553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483a94112583ff9c6d0a7b67348fc3b0ee5bbf104a86a9e24585c9ad1028fd25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:54:17 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:54:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:54:17 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:54:19 GMT
ADD file:5430e0b4ea856c760b6e2b88e8c2cd2d49704ed2f3c53ae34c10750a608d40ec in / 
# Thu, 30 Nov 2023 17:54:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:767829bcf202e4fa7e777f29d390307e29ac437f131685a1ff1293d44705ca23`  
		Last Modified: Thu, 30 Nov 2023 18:06:39 GMT  
		Size: 27.3 MB (27273553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f5ac92fb1f602adf15449871e0593a7b38f7a461de589810bd887e49928ee62d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25203103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c99846a5ef249a3f390310f0283176cee9c661d1221d866b942b11f50ed31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:34 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:36 GMT
ADD file:f2094c969cf67a5474ae23a10eed122a6aa80b1fe7f01fda1a770b8fa11f8a98 in / 
# Thu, 30 Nov 2023 17:41:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:081b2ed8534a247171d83183d75e8113b3237c45f1b12933b7d6833e80a58198`  
		Last Modified: Thu, 30 Nov 2023 18:06:52 GMT  
		Size: 25.2 MB (25203103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:694c2aa053066101c5f29e909d4baaea478ac50e499d452f510c10e961ebb42f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26391312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382e20053971e462c74b86d6dd56f440693ddf596f0fb4989a9ef87ffb1bd5a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:41:07 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:41:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:41:07 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:41:09 GMT
ADD file:973e000ef2f95dfa48695815ebd7027db718c9fe80260271e43ee06fddfd073b in / 
# Thu, 30 Nov 2023 17:41:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b227d7805fb6cba5d091f0565054ae9ed1e13a6e2df91de4cfb41f70e208da31`  
		Last Modified: Thu, 30 Nov 2023 18:06:46 GMT  
		Size: 26.4 MB (26391312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:22c4449e6ef2d40adecaf8ecc4df1bd80a701c12f89f29f15245189cd3da22b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31346558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eab81e5b01a3726fd0cdbe70cf8d42317086e71ef61ad68667b29af27db455b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:57:33 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:57:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:57:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:57:34 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:57:37 GMT
ADD file:d08e45288fbc31570a3a92ae480bf6ac3ed8e4900b3260d56a51ce024818b6fe in / 
# Thu, 30 Nov 2023 17:57:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86fa66fe8d0305c6369ae9bf03d1677c1d99b5cefbef6dd550617a300956d5b6`  
		Last Modified: Thu, 30 Nov 2023 18:06:59 GMT  
		Size: 31.3 MB (31346558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:f9bd1296086163c80f76427fb987a4ecf6799b490c724fc0bea92e66d60620cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bd2cee374af30258d9d818b2ef084ef72674c8a1304bc94b177dc70da33166`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Nov 2023 17:42:50 GMT
ARG RELEASE
# Thu, 30 Nov 2023 17:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Nov 2023 17:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Nov 2023 17:42:51 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 Nov 2023 17:42:53 GMT
ADD file:63283c7c5d335fa063fe3da82fa78d45ed5af9327a2d154bad18a8711485db77 in / 
# Thu, 30 Nov 2023 17:42:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5ab01e9ae41fd34fc412118be6d5e21f82290394cf86ba09cd54207fa341e2d9`  
		Last Modified: Thu, 30 Nov 2023 18:07:13 GMT  
		Size: 27.1 MB (27094013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
