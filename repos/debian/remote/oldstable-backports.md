## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:4497fcdaed8af40794e7b1120a3633f3c7e54154efbe567f0f2d96ed45d5426b
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
$ docker pull debian@sha256:8baa353f0619cc85caf6b80dfbccc6c9e2078c261fbfbbfa9023887efe19c535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39bb6b9bcaade0fe461f5d1fdd879ceee35286943ed578ee82f276401d58349`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:23:06 GMT
ADD file:e1b6fc4fae406f15c838d9ac376bd11c220330917467e8d51fcf579828fa9826 in / 
# Tue, 29 Mar 2022 00:23:07 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:23:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d56c2a21d748d59ba00ecaeaac18def477f99dcfc438671734baa7248a0b588`  
		Last Modified: Tue, 29 Mar 2022 00:28:56 GMT  
		Size: 50.4 MB (50437921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bb589e54170d7439bc444903819b002b87e6feb05c6c02f7170d17742a7ca`  
		Last Modified: Tue, 29 Mar 2022 00:29:05 GMT  
		Size: 225.0 B  
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
$ docker pull debian@sha256:df07eaba7684af4416a4586a8e5e2eadd793b5cf9e78c82ebc4294bff6a1976c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30c37c70cdfbb479b0ba26f3350ee7410ccf28b7f759f0e91d4f6f7a018995c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:33:33 GMT
ADD file:395ce20dac2bd94688a9dd481222d5279410ce7cd1a3f4ae1eea631c3f49cc2a in / 
# Thu, 17 Mar 2022 09:33:33 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:33:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a00a2be74d30413203cd0c72d41dde557e12f57905d392401bab26e4ba0f92e0`  
		Last Modified: Thu, 17 Mar 2022 09:49:48 GMT  
		Size: 45.9 MB (45918164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702d04f9d8dd6470c0f9167ff4d71381700e12102944c1dc87ca63efe993430f`  
		Last Modified: Thu, 17 Mar 2022 09:50:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e3fce25b401a021f59b30ef6a8f8351bcc2ab46156af8a03455a0c9e5038bc82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49226045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b9996e896f7a4759153af0a56e04d595b17c0399e5995156e347e3aec48516`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:15 GMT
ADD file:000e42c0581dc2cb247d83126de1b4213fedc2cb838e7c8b5fa6306b10316cd2 in / 
# Tue, 29 Mar 2022 00:44:16 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:44:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a93a0cf87088be1647f70edcb8d320a86f12725cc113afbe5141c1403fb66e30`  
		Last Modified: Tue, 29 Mar 2022 00:52:00 GMT  
		Size: 49.2 MB (49225821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054224e0c254b49bfd7cb574b7d9dae05f1ff80d3d1f361328adb967ff456c24`  
		Last Modified: Tue, 29 Mar 2022 00:52:11 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:96ab65094f23a278709492e8500a406cf38f1fdefef8cd7c0e309ffd7f437385
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a5b9a738c5af015b5294a418e4ed268d4bf0f77e26a2a61f1ef468cac61bff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:54:41 GMT
ADD file:41bcb19aa2a6925b18a880af7a7e39bbcda297219288ee55dc9780b5922f5377 in / 
# Thu, 17 Mar 2022 08:54:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:54:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7c6ce6359b3d8d3857b088c56fe16bd48b385032bc4ecd48dc843839daa0475b`  
		Last Modified: Thu, 17 Mar 2022 10:45:21 GMT  
		Size: 49.1 MB (49079438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4bf93fbe8db05e51eb4742b72a1eb2200add805af38d396e71d7828db63ce3`  
		Last Modified: Thu, 17 Mar 2022 10:45:30 GMT  
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
