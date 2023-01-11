## `debian:stable-backports`

```console
$ docker pull debian@sha256:36040473d82d9afcfcc02a87bad260e3ccab8e4bbffbb06513df55eee70b89a8
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:fda18ada771e6e46f59e754497ed3be5e2e899b8183f01276a7070d4a79bd50a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55025387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b694b6b32bcbbcaf2def83d6c748bb1a40538015fc3fca7221eda039901531`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:36:02 GMT
ADD file:225598127787c3bb9629bd64dff9fe139f1fc5c206e6d0cd7ae5aa52b5fe11a6 in / 
# Wed, 11 Jan 2023 02:36:03 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:36:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a58c4afaf5a14bb0b7f44c8cf6187da3ef4a649ca262285a266e0cb84c39a126`  
		Last Modified: Wed, 11 Jan 2023 02:41:09 GMT  
		Size: 55.0 MB (55025164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779b772574e95f418dadbfe06022f5f6220f121fb22dceba7e745a4e84917ea4`  
		Last Modified: Wed, 11 Jan 2023 02:41:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d62fcf11c55c2ec1e0968eafc7f9a31405fac6cdd102ee6ad1503b7c448f8cad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52530215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8a51e1e2981c73ff042679a703c2e4c7599ab2331f531aaeca0e712aa11636`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:56:10 GMT
ADD file:237196db53217608742d987c4a09af8e0db3fd86650a33f61a89c52b6c18d6a5 in / 
# Wed, 11 Jan 2023 01:56:11 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 01:56:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7a106bbc20ec9dad8c8e629f85849a2d05a29d1a114aef7dd954abf640aec746`  
		Last Modified: Wed, 11 Jan 2023 02:01:44 GMT  
		Size: 52.5 MB (52529992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a0499e52fda338c6dbda7dc1a22cef899feb9448894c5b0da9d7857c9fe16`  
		Last Modified: Wed, 11 Jan 2023 02:01:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3690b35e6c134f8638388806fbfa41b32e6389f7d3def9cf323ac633b2308fd0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50191027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2adfd450c7b94b1d355712b444c660155968e73991577f6273cb6e4bed89c65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 04:02:28 GMT
ADD file:f4df120a784b31b157b607954568067f17c3119ac06e5e450bbc596f797daae1 in / 
# Wed, 11 Jan 2023 04:02:29 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:02:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4d5da366d02b51805b70c4fdaa7e9667e2c1db0ad20127b28976166ebfa5349d`  
		Last Modified: Wed, 11 Jan 2023 04:10:22 GMT  
		Size: 50.2 MB (50190803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8facdfd7c8c0d17198799f45d53d0139a928130176f6b99ea5bd9838dfc612`  
		Last Modified: Wed, 11 Jan 2023 04:10:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d0ff86c5cee2a0c87b948e8b06b027d519d07f8494fe287ab2d7de9f1982faba
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53682033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970412a413a4963ed86e583f6ad358e791af874f0a50de5bb8dc565a7a323de4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:58:29 GMT
ADD file:b3b3fa9311e6fb6fad179e3b9922a16d882cdb013381d8b1a7b0e02298fa841f in / 
# Wed, 11 Jan 2023 02:58:30 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:58:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:215bed8c39d4f4f554fe94e4bc572246d947f2c9d9ddf776b5ba590ee3b8f27c`  
		Last Modified: Wed, 11 Jan 2023 03:03:16 GMT  
		Size: 53.7 MB (53681810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373827776857694ef3909ab86e7408f7f6c2547f85b162048fde8c0a9619ec0`  
		Last Modified: Wed, 11 Jan 2023 03:03:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:859ff136a3a2ea34df1d1e773c77ff2d94db6941286d9f1e8a53d5c9401586ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56005529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa2c2f74b2cbdde676496b0536ed3b4dfa92d88fae3cbe7dc649dc127e024ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:17:38 GMT
ADD file:8b1ab50aac7fb620203a756c828f812a24b020a71a1ff7d4ce8d8582b1504840 in / 
# Wed, 11 Jan 2023 03:17:39 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:17:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e73f33a0d99bd0f825ca24faa4aa793a3a3b5e1460f7b3b4d1d3d448e296bede`  
		Last Modified: Wed, 11 Jan 2023 03:24:19 GMT  
		Size: 56.0 MB (56005308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4959daece09dc024ac8131a710565883d10ca3518f6d9811bebac9e793c6f204`  
		Last Modified: Wed, 11 Jan 2023 03:24:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9aab52a589fe9adb13fcae676a04bfae7b99c57300e7cc8a700dc807dfc78502
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53245305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1625ba8424f4f61766c62a44446a217c11a7d2208c23a61833205b56486ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:12:11 GMT
ADD file:c78307398a21ca1a1eb99dad7c1e47578e8459d4a935d7f9d83dba7df1982d97 in / 
# Wed, 21 Dec 2022 01:12:17 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:12:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06854a7b3b78f7102b75c303383d67d86ada6d9dff67c9ee5ca3200abeaa24f6`  
		Last Modified: Wed, 21 Dec 2022 01:20:35 GMT  
		Size: 53.2 MB (53245078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c90e6970b771356c4b72159d74bf6b3a025f3cceac9fd0f3b8747958bd15dce`  
		Last Modified: Wed, 21 Dec 2022 01:20:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:dff5a104d8fe26b97460de19363d404111f0b1f17f5a113e0f077e32b5f2dd43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58897358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f576d9b4efee260dfc72bb2e5b28bd2de465bda99d9f8480e7ccab1dc4d44a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:50:29 GMT
ADD file:98e69a05e1f64cfa0e20e89cfa02441667a95bc336d8e6488cdf6bdc80a5e0ed in / 
# Wed, 11 Jan 2023 03:50:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:50:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:811206603d3df9301628e360160658d712ed2ff25d1a41f807a40776c5fabf96`  
		Last Modified: Wed, 11 Jan 2023 03:56:45 GMT  
		Size: 58.9 MB (58897132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e0dd3d12a50613929f09426926e9f84173190f7134b07c8b9c9111d395a39b`  
		Last Modified: Wed, 11 Jan 2023 03:56:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:a6015feb567a8fea42275fab93ada27b11702e999f27d7da6af220315f29d3e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53258712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dcb05ea6c2f75724e0eff9624550bf2de0cc61f220e5d9032b8d8290804bff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:23:07 GMT
ADD file:5fbb251abfcf0720f358a041c82c803c587e7bf78a7210006b304e0320b9331f in / 
# Wed, 11 Jan 2023 02:23:11 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:23:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5fb163ed85abeec4b8d6ef35e8184d48de4bd3a463cb58f2f464c956be56ea8a`  
		Last Modified: Wed, 11 Jan 2023 02:27:32 GMT  
		Size: 53.3 MB (53258487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3f81a32e8acd62077e2acc78496eb5d20a77cffc07417cc7160a6d937a255c`  
		Last Modified: Wed, 11 Jan 2023 02:27:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
