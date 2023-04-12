## `debian:testing-backports`

```console
$ docker pull debian@sha256:f29977ce9adeb1dd9e31e1e64bbe17da6838fa60958ffb6352012180e2dff3f9
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:fe19c4b2d059c9ba36f599f56cc788286df0ba9b78325c71c64439ef99a9c360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608a475ba8f8dced199c0e628ef0b6bfced620469d35bca538293a8c3a4ddabe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:21:33 GMT
ADD file:28aeff48a52e156907bf710c1e3cd7ac329d157f36816ca755bcea5177269765 in / 
# Wed, 12 Apr 2023 00:21:33 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:21:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c6654873ad3f068a7ff34cc7f44a13003d6eb6f2261ac42d1cac07ac8ed4e0e`  
		Last Modified: Wed, 12 Apr 2023 00:26:11 GMT  
		Size: 49.3 MB (49292939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf6486178d1f01e7f1887374d4f74962578798dd9a755349d4b4bfd7e78af93`  
		Last Modified: Wed, 12 Apr 2023 00:26:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ca311abc1ce4ea3dc5ab853287fa8d4b54eb39180a38f937f5ff3a7da3f2fc2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5262965ba2a3ee40583e7f1da6aa13f45df50d3f793385aa7ac1a86c34b2e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:49:15 GMT
ADD file:85dcd54a50e4d3eb3c9fd82aca6d66cca88acded747c1da4c93ee576bea87711 in / 
# Wed, 12 Apr 2023 00:49:16 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:49:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f82b37ef52e32206315f11aa91a2775f8a9b2c6ab1c8254df326ae0d47f9d5ed`  
		Last Modified: Wed, 12 Apr 2023 00:52:27 GMT  
		Size: 48.1 MB (48110880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77525a987a5d4d74b8f70e7761301cc8819ea87d88c3ac56ad51978b4e4f7cfd`  
		Last Modified: Wed, 12 Apr 2023 00:52:39 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5ebb536b168ceae4727bc22e09fee738989afab42dbb3955a2d607ecf587717d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45883337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f49c7e6757bfcf5dd6bd0426b8037236fbea6d680c5f0f6f4cffd7b0d5e5f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:11 GMT
ADD file:644c1d3ee017b7c76344e5dba5070a3e6fdcaaee9c73c7533f5a8cec8df4c6a2 in / 
# Wed, 12 Apr 2023 00:01:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:01:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df24a1290fa20d99e5808e99b1da79324d929f1dd276b232f75c3f5ba9fca816`  
		Last Modified: Wed, 12 Apr 2023 00:05:44 GMT  
		Size: 45.9 MB (45883115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42d26ea6848e711a92bf0082d3e5ec7ee9283a4363324184899219dd26d43bd`  
		Last Modified: Wed, 12 Apr 2023 00:05:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b958a8b8c944c4c932a8809c5c9761efe58c0aa9c8fc20798933b3418b50b86f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49345587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df509ee94bba241f03867afa48de9f523a716eb39d96422153ed75c2a38844a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:46 GMT
ADD file:80a4d0d891f9f28bd3948de18579583b6c11a4a8805b6230daaa0ac2a35c453d in / 
# Wed, 12 Apr 2023 00:40:46 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:40:49 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1d33b0463b9cb723855fca4aff8cdc62c34a1907b920e8e626bd38d7577387f`  
		Last Modified: Wed, 12 Apr 2023 00:44:53 GMT  
		Size: 49.3 MB (49345366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824085549218ea0d8a075e376c040022cb0bdb5d2c70f355da9f5b74fdc5d64e`  
		Last Modified: Wed, 12 Apr 2023 00:45:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:7edf9294de1de7b9ad7f6d3c42c534cc8bdb5b8d1f48aede33b65fe2f1ed2b23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50318202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4194f8228761d780442e0a8debaf02abb06e7bcd6a1f08b3e2d9dff716a15a43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:30 GMT
ADD file:2ad0fad15fbda4c0b699b4aaa14445b0322d2e2271a4b3fbd040b3e84b7d2ce6 in / 
# Wed, 12 Apr 2023 00:40:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61d509c5edb6b6fdcff4f76f6dc24de7a3b1ff8b4c805019cb42cc6720e0ba9a`  
		Last Modified: Wed, 12 Apr 2023 00:45:36 GMT  
		Size: 50.3 MB (50317978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186698fed537745de84b7a675eeef7ba18d97de9b88d00d2cc057ad83d114324`  
		Last Modified: Wed, 12 Apr 2023 00:45:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8f9cba228d7b0642ff42b1ebc812027d7c394ecfa5886abcbdf4b42812a1fc4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49299545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a82a9a8007b3b23b73a4f3bc93e2875334105d537eaba6f0c076dd410506e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:12:29 GMT
ADD file:c8ac2734abc43d5debc82cde3d350a41bbdb9839a979a975bcf3c0463e954234 in / 
# Wed, 12 Apr 2023 00:12:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:12:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:49cd33eb75d2a83e7f320ce1efc4ac9f56141ad9006032934badc3c04ca429d6`  
		Last Modified: Wed, 12 Apr 2023 00:20:27 GMT  
		Size: 49.3 MB (49299323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d6af93b238ad0986328bb1deb431d254d2df5577559183b3058577a60e634`  
		Last Modified: Wed, 12 Apr 2023 00:20:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:96d7b54f0268962c06529af3d7a7e5ff47172d33d6bd7cef62f240b57d688561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53300211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d22bfb580d41af378c86caac475266f2e64c5d9d53d80df106cbbdac63e0eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:00 GMT
ADD file:107d4f159f2bc5b04467e08852422f5c78548e0f92853bd29d5d2b05b387d3a9 in / 
# Wed, 12 Apr 2023 00:10:03 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:10:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4fca5aa8bf3f9957686fb6705daa645629edb94592f35c71e46e52a1742ed1a`  
		Last Modified: Wed, 12 Apr 2023 00:15:06 GMT  
		Size: 53.3 MB (53299985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a64bf96cf803ffe2505fbac1e0c249266e23f4901c9f082ece5ea0af9c8361`  
		Last Modified: Wed, 12 Apr 2023 00:15:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:8ac017a8c6eb467c9ac5140e50fb9481d203fc191eddc7de9142f439c8ca8e71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47670629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ccb3922ba228fb9cb3d2d4b1ad27f87fe6a2301c2c337986cf5610d264c207`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:02:57 GMT
ADD file:a04191f521f5135016e837ec503a63f4e8488c1a13030ba67c96cc8f68da9d50 in / 
# Wed, 12 Apr 2023 00:03:03 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:03:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0d66e85e2f078d0a3241d6085f175f28d3ed3f6304a2561cc20fd703234bd4bc`  
		Last Modified: Wed, 12 Apr 2023 00:06:14 GMT  
		Size: 47.7 MB (47670408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d306832faddd6ad34c518e489793391a11865755e5a2f833e5cb6269f39c1`  
		Last Modified: Wed, 12 Apr 2023 00:06:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
