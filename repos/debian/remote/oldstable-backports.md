## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:2eed4ecf984128144deb993e4d9b8737071442197cead489d2529b33f26ff14d
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
$ docker pull debian@sha256:96cbe179bda137453706c2fb1bcff9791bf7954502e728fa76eb12b4a61f3726
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d00394c540c916c45931972a9321db681bbcb0066c0954d6f37727b94f7280`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:44:17 GMT
ADD file:8a4f1d7e5e52aa53b75f2808ce11c808a8e77c6404891742f522fb7a7e986f37 in / 
# Wed, 20 Apr 2022 04:44:17 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:44:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c45c7abc4a6b3c318a73fe816c8198b2491c4dc321a9ac23dd5ee43d702623fa`  
		Last Modified: Wed, 20 Apr 2022 04:50:13 GMT  
		Size: 50.4 MB (50437032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b310eb2a533b74f3b684fae98b6af97bd425384fc31bc31856ef9557a5ffd74`  
		Last Modified: Wed, 20 Apr 2022 04:50:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e70125e6ccb80c01ad82e9d5df910191813ee6440d30479c44347614a8af61cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48158551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b88d38673434c78c589d35ab4f8022ae3a02b259c41516b8e27e48d07f0fbdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:57 GMT
ADD file:2d960bc0287622d1670df9f6e0da1822b454eaccf53cd64b67a8709a3b4e9f28 in / 
# Tue, 29 Mar 2022 00:52:57 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:53:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:201a098059a97e21ead04f2c365c915c4375140d17e44f74f9e972663a897986`  
		Last Modified: Tue, 29 Mar 2022 01:08:49 GMT  
		Size: 48.2 MB (48158324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe93c928feeed602420fa1c301d1896a9e69bd060fc109ddd3cfecfff996ce0f`  
		Last Modified: Tue, 29 Mar 2022 01:09:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:aa244641b77ef5dfde72983f30478ff7f5302053790bbf82e5377262637407db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45914783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dee576f5e8d507c6454a001e9dcc5812158bd5fa30da519a0c61268901cee51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:21:06 GMT
ADD file:6eb791ed26da9f66900c8910f26852b98d89eff857c3b311da8cc84ab2c1fc6d in / 
# Tue, 29 Mar 2022 02:21:07 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:21:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2c3d159380c9c644e808e974c1a8c35f654cbb83a1efd058d01343006270c2f`  
		Last Modified: Tue, 29 Mar 2022 02:37:17 GMT  
		Size: 45.9 MB (45914560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa4e71ba95ce6c640965c2257e878dc526e668abf4450ca3292212cf09b951a`  
		Last Modified: Tue, 29 Mar 2022 02:37:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2cc0a75cc76b25edd5f8f5125fb35300d64aa8c3bbe5623f25d471c640f3a726
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c2a64e9ebb6d4acc67c28de26324c208f6a40e50a89548a9209d30261e08ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:30:12 GMT
ADD file:55626f1299c943934f8cd38ec9a9cde4d4b8beede74a23774f4fe6ca0b7ec45a in / 
# Wed, 20 Apr 2022 04:30:13 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:30:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d6f4a9b5619dae92e0d604298044fd2a8ed8c396fe01e6ab40d3f2bd5605473`  
		Last Modified: Wed, 20 Apr 2022 04:37:38 GMT  
		Size: 49.2 MB (49227718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d06947fd270084fb3f4d8cbe2dd6f4b7b7e3ea4b15b9ddce40569f59960f5`  
		Last Modified: Wed, 20 Apr 2022 04:37:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:df46ad8ab8cdc6d7e34de3e5e15e15b052b75ad8362f437dd8b5134e45c5b2b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa39b37834d257c66a60e1c206585ca9eebd6d2449f851d9e48ef53d060e801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:01 GMT
ADD file:1109681ba098fbbbd9a0fa81b5062cf1555056960e30ff4fa4560c9b5672760d in / 
# Tue, 29 Mar 2022 00:43:02 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:43:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2e1a47ed57b272a979971a2939a528c2bf7677e5e2be48d40492d0b03066bfa`  
		Last Modified: Tue, 29 Mar 2022 00:51:07 GMT  
		Size: 51.2 MB (51206653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f092c73238606ab48327353a5d755394552a6cfd12ea5489645b2ee1a0bf0b6e`  
		Last Modified: Tue, 29 Mar 2022 00:51:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:195cfc4c88e902d9fd7799b55c56a54dc4440d0756a646378d2a4c17b581b763
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49080099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4f643d413d25802e663ee90b69ccba4a8b00d1502dcde33ebda8e98951edf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:44:08 GMT
ADD file:2d8c34802d0b44aabd27e95eff2ce94751098f2cc68aae7f789185fd8aae0d0b in / 
# Tue, 29 Mar 2022 07:44:13 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:44:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bd194f847b7470ac501b6bd3620e76ed1178f748e2cdc221ee013f7d5c74b72d`  
		Last Modified: Tue, 29 Mar 2022 07:55:01 GMT  
		Size: 49.1 MB (49079873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a3c96700fbe540f5b46f50c924617ad1e1b8807c5af7c41c263a598e31488f`  
		Last Modified: Tue, 29 Mar 2022 07:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a3cc2fbdba92309d6fb9d365e4cf73196181ff35fd87f48de74f1d0f0fec9b1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc930844852cfdfd4ef1dbe03eca71559dd71fd6695bc905ba1c3b2bf9c66000`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:23:14 GMT
ADD file:9c2cefc0e76c6d633a2239ab2c7e162d531b8addf73f0d6fc319b622057b1f52 in / 
# Tue, 29 Mar 2022 00:23:20 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:23:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ab9f5ee84078ff84d542a6d7e6f4cd5716c068a37d22f538a5a48e157acaf19`  
		Last Modified: Tue, 29 Mar 2022 00:35:34 GMT  
		Size: 54.2 MB (54183146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df7824820308541228dff17430ed65b5426ee3bd5fb00cad33d5e2586459f68`  
		Last Modified: Tue, 29 Mar 2022 00:35:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:2cf5e344d0323759487a3c94683f54111603efacbfa1764691ed9d9a50de977f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b1ee5a6c5fae3d143a82022bd41cbaba376c22eb9b3f2e11b29b05d967154f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:39 GMT
ADD file:6b6aaf180e1767d1ffe0ffc10aafea968cfa30bdbe43574cfef40eb9a3ad091e in / 
# Tue, 29 Mar 2022 00:52:41 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4e41ede1772ecf2953e91dc77874f400b87f5eca743d5783eb764499f7c1d927`  
		Last Modified: Tue, 29 Mar 2022 01:13:03 GMT  
		Size: 49.0 MB (49007766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dc763c4b85cd79e3df035bacc500b77e2808bd232bef2d78c3d712f543d248`  
		Last Modified: Tue, 29 Mar 2022 01:14:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
