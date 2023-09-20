## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:2a50d3d136d14174a6faa65ef6266ff49304adae28efb7a6896d779e79d28344
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:ef429668170f94b752556285d9b98d453dd69c2ca7fc8955948face61eecdd4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55056490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62020abdb37310ccbb46a2b5fe0580d129ee9b344e3008eaf824458b0fcaad13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:22:05 GMT
ADD file:52cff30f892389172481cc0359bde2ed2dd4acf4a189dd57c1f56f407d9b3d7f in / 
# Thu, 07 Sep 2023 00:22:06 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d16c0ac7be786ecfb9fb46c48e4dcdcc40afa63d97c1904fb6088e23940309d`  
		Last Modified: Thu, 07 Sep 2023 00:27:35 GMT  
		Size: 55.1 MB (55056266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25449fc52443cf7c7eb0db7ae3189bb0f26571cc80f751cf106cca2908cf538`  
		Last Modified: Thu, 07 Sep 2023 00:27:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4386958b015f7e44bd738ec9710928c4faeddd65d50fe1816273ca03abb9bb68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52558398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825a2d2e14dc9c06d92736da5da3ba08f9e249ac0c03e784080641e592eb6fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:50:35 GMT
ADD file:6585afdc8b7840bcbfa96fcb0bf0d7d7e9eb5539dd1cec70e5ee6f31209ad3d3 in / 
# Wed, 20 Sep 2023 00:50:36 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:50:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea4d6080a0290f592c439c3add7fef2662b6e325c704d049e34f299626e409dd`  
		Last Modified: Wed, 20 Sep 2023 00:56:03 GMT  
		Size: 52.6 MB (52558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4209b7809d4853aa26fd899302544e9e1180418b029b1ce42bd978582e9dbf05`  
		Last Modified: Wed, 20 Sep 2023 00:56:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:523809a34b54a8de51cb96e2e23d9ebd9b54f541c62bd4c20f9131e30a2adcff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50219432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878d23ee51b4857b0193ae07b791f9074065241362f47c1ec8293e079b1e5173`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:59:08 GMT
ADD file:dde253d9c1302aa0f98aa4e009d679edc1477ec26433508aec5adbe7194529e5 in / 
# Thu, 07 Sep 2023 00:59:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:59:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:995a6f506d1800e9da0998564c6bf44de76a9ac7b9ef77facfd8f5f5983e3703`  
		Last Modified: Thu, 07 Sep 2023 01:04:46 GMT  
		Size: 50.2 MB (50219209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed31519919b6228e52c0501ab65d120fc1d9eaa851e88c35e1950f01c8fd9734`  
		Last Modified: Thu, 07 Sep 2023 01:04:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:930af8b2c2a26f9c7dfab1c39d8854129224e3a93b48ba9eb5febfad40cdfe14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53704953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabc197d00d4b0c38c0a1125c2227dc0100627c1e47e26cd0b8d7d0b5a8fabbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:27 GMT
ADD file:50b2349c912d8b962881ab114daba10d3b77be00595ba001336712d3c5b0c38d in / 
# Thu, 07 Sep 2023 00:40:28 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3a0700d78826dbeb364ad798c94314e4a06d7f76863becf5bc231796fa5aaed`  
		Last Modified: Thu, 07 Sep 2023 00:45:05 GMT  
		Size: 53.7 MB (53704729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3068113f90d8703f011dab78b499b84d0302c0269d82c10fdf4aaa39521c5132`  
		Last Modified: Thu, 07 Sep 2023 00:45:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4ba1e830424d3a22ddde701827c75cace333d24ebc11a12962d85387bcae17cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b63c27a3887663d71b353e811a74bf4cf99096ed1b86d514f781a8ca6ea2bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:15 GMT
ADD file:4972d10c6107fd20bf98c1c94a441e2cb3d14a625feb9e293d0b7527d3c8efbf in / 
# Wed, 20 Sep 2023 00:43:16 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:43:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73d05fbd9bfd3b656f84a6e1bc2e910f22de1d965198a98739ccd97ffb57a9cb`  
		Last Modified: Wed, 20 Sep 2023 00:49:26 GMT  
		Size: 56.0 MB (56040484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508dc8e0165a6fa72f96bd91e0c60ed4728c023d52bc243d580fe6177926b06`  
		Last Modified: Wed, 20 Sep 2023 00:49:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e12078c60f33d79020ce435a363bf5e3f2b548de8915573f8c86aade466f69e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c669bbdacdc88cfe2284a5fd39ef3dfdd63eef641d0dbbf7208ed82fe89bbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:11:00 GMT
ADD file:489997b60e50b54d0265698dafcf27c8b0c9ceaecbe9ffcf5314ab78e6e09503 in / 
# Thu, 07 Sep 2023 01:11:06 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:11:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3a43a145c5babf476f66ff7a5660dd356b3182765df9a6f8a95e448e8c5e5492`  
		Last Modified: Thu, 07 Sep 2023 01:22:25 GMT  
		Size: 53.3 MB (53271475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a172a9b2ea7f926dcbb9f37814471948cfc9186c8c41f65ffa9adb539c3c8b`  
		Last Modified: Thu, 07 Sep 2023 01:22:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:93c0759ecec4d18a0fb20524d6b7855eb6ae8be567e5e2ce93186143ecb938a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58928346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad90ecb4e4702b0db3da8d65f6faf2f3d1f183a13e0c814b152fe57b0aa49c7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:22 GMT
ADD file:e66bcde662505500cd1c9ac76d9ae76cfad59f8cb57b4951c4bf0aaf1c951b2e in / 
# Thu, 07 Sep 2023 00:18:26 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:18:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e4b9a8f54cdd852a98f3fc55d957ab3de7d2430e8ac65164b7b0423bd976387`  
		Last Modified: Thu, 07 Sep 2023 00:24:51 GMT  
		Size: 58.9 MB (58928121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b993fdc85c91c6d40b687e1ff315e05758791494fe0a669a14a8e6689582b93a`  
		Last Modified: Thu, 07 Sep 2023 00:25:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:9b7252052f31ea1d62b3c7e2afbca9327dddcead5d4570a95e79228e2ab775ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53290440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573109558aeec3a1d67c78544096383c0592a0e1ae53cc9cf1f36431056bbb58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:50 GMT
ADD file:ba73ad1120c7048bd34f6f7dd55f6746a346bb368074b3b30172b5c9a37db7b1 in / 
# Thu, 07 Sep 2023 00:44:56 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:45:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:19b65a2df95ea239d5295384110e0159722b658a74231e5f641738126fc1fa3b`  
		Last Modified: Thu, 07 Sep 2023 00:50:24 GMT  
		Size: 53.3 MB (53290213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804294cce10c5414c6a32b3f3a8c495008d4539f37e571403dc1fa38bc94b586`  
		Last Modified: Thu, 07 Sep 2023 00:50:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
