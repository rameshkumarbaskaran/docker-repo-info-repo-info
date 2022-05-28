## `debian:rc-buggy`

```console
$ docker pull debian@sha256:5b56616e9250794c7ad2a331a3712f0898cd8856358126fe4539a4d21af030a0
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:fc23ff654c6289e1553fe470f167600b2b66de1709ed5f3a1a0889105dcbaab1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09d530282fc7cfcaad88437041896cce979e443213939c9d4f05ae716d2632b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:21:27 GMT
ADD file:365db4cb0be9894b5b688c566f8cb6ca848aa3777c680189478799ab75fb4be5 in / 
# Wed, 11 May 2022 01:21:27 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:59 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cf4cf577d743a8a18a793a3887db0f30d2d2093715da6cdfc0d68ee62f6b790a`  
		Last Modified: Wed, 11 May 2022 01:27:29 GMT  
		Size: 53.1 MB (53147126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155323335cec8340f923f93a9370f05b546640b62e521cb6b3eb58daa9084328`  
		Last Modified: Wed, 11 May 2022 01:30:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:917820f1fe302b56467bbcbd693539ebf3d438f538d38afc63c3583fd13f7f7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50940059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01e83b6fac36db5aeb7498b43d76132e51fd36ffee63ccac59de218b4696780`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:53:50 GMT
ADD file:4f142f5aefa97fb474a705d0b74abadc5a3efdc7faa28a865e8f774b46affcfa in / 
# Wed, 11 May 2022 00:53:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:58:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d1faa3808d790c86a331ed5dce0a7a8af6a26aa395d982f287f5d3fe6362186a`  
		Last Modified: Wed, 11 May 2022 01:10:36 GMT  
		Size: 50.9 MB (50939831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9690c9d6869f0e146db789a53a2ab5d60825ca265a823e7fd6354b05a0ec2`  
		Last Modified: Wed, 11 May 2022 01:16:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:1e226eac1618fc5bc33b903b65ca601b8342b9e07617f44767e1a26d2780db2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48678528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1134c23f13b77bf86ba9def7389913c6a67e506bff8ea50fa993433c63d42ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:52:42 GMT
ADD file:5256a3df37de011e57faaf3b387bbc66fc94fceb82c48ead6b9e5775cbe7bf21 in / 
# Wed, 11 May 2022 01:52:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:57:30 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:528d9ed2cb56db465cbc360f474c45ab8e5ae05c0a0f596fae936fc1290bc68a`  
		Last Modified: Wed, 11 May 2022 02:09:01 GMT  
		Size: 48.7 MB (48678301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7d1a35b7785333b7abbd57cb2cc3ff8de5faa54e74f0974d219b832a0765`  
		Last Modified: Wed, 11 May 2022 02:14:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:99429a692c76b00d96a37ea1ad6c2dcaa6d47047e2b34888a60b6fdd0cb9dd3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6e19aaeac0e389346a25a0907a44711cb3fa99b0f29a527dddb89f98d618a8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:02 GMT
ADD file:759f672e6b6df1008eaa41bb27f3166127eb98b40bb49919dd41fa53f7e9d598 in / 
# Sat, 28 May 2022 00:42:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:eab2172da7bda865d054e2983e44baa941cea4422c5c64ceeb52f19efc8e9a16`  
		Last Modified: Sat, 28 May 2022 00:50:07 GMT  
		Size: 52.3 MB (52261302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14192d76a4a08a40688357598b1fcf246eb8922673176765bcfea0e585c9edf6`  
		Last Modified: Sat, 28 May 2022 00:53:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:94ccb245b576b501331506350eaa0feb0da151a2667e7f649ec7acdd0c466230
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54158944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91615f672daa741c0aee0f743df7985b287e3740bb4308bdaad3dccd3e81321`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:03 GMT
ADD file:dd10bdbf07bc13b42a7021b48621548cda7b383bf0edb8dff1e35d908f50c392 in / 
# Sat, 28 May 2022 00:41:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e233042357300fc1ac460e8583f90e2b88388d7c2a9016f91be99da315c46fcc`  
		Last Modified: Sat, 28 May 2022 00:49:18 GMT  
		Size: 54.2 MB (54158716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba5ad64f8c5ed67f59112c69f772bc1553a1e013a3611c6c558f44e98052a79`  
		Last Modified: Sat, 28 May 2022 00:52:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:ecfe349f58a3a1013f61d8ee9081bfaadc0d8c68225ad1a20523d68738052b43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52268569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9df5b2283335a37f4d7dc623c1fbecd4bb813c4e2c739ed885a72b43fc2b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:26:20 GMT
ADD file:6fe62ed367eb3d2edf1db05997b04ffb1d77dfe3040a730186cf442070e40212 in / 
# Wed, 11 May 2022 02:26:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:30:29 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a63c80ef33466ffbd01ed95c3264ba9bdec7ca0346e5abec9019f90436d8ed40`  
		Last Modified: Wed, 11 May 2022 02:36:59 GMT  
		Size: 52.3 MB (52268340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acad1795abb43d00eb93a8dc2a071c5b84f823500e644c1d768816f773ecb1f3`  
		Last Modified: Wed, 11 May 2022 02:41:24 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:a7ee35aa136a3db0d80388ee26287502016a2f7b63484085b8d5bc0f58840cd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57352590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dc74008bdbdfe790ed567327fec29cdc4266f985d12668ee0a91eeec706abe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:35:07 GMT
ADD file:7d4f085f5fc874b6142d1d0a27c78512d764e68948baffd110bb6e1ff77c725d in / 
# Wed, 11 May 2022 01:35:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:38:59 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6f5d4115fab6dd67cca7bafe684609d704cd4e4c3229c7f62f0f1476fe5cfd02`  
		Last Modified: Wed, 11 May 2022 01:45:26 GMT  
		Size: 57.4 MB (57352362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cf1530628350940b2a5a68024257f66e97c42e9af1dfca0a865a99aa97173b`  
		Last Modified: Wed, 11 May 2022 01:48:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:62f79cd3374aa69a0e21069e6f082c057551f1770676a845f7f287cefc3d6ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ce9ebfb788ae8cd919db4460d2c9120f0db7770f4f5553dfdaa6a542bb0a60`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:44:37 GMT
ADD file:03a528116badd98d1660ab1a83ce0462a11168a2dae972be4891032c54483f22 in / 
# Sat, 28 May 2022 00:44:41 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:46:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0cf941fb152b37e3fda284ae5eceb3dab36c26511fe06a7105ee43081ca68554`  
		Last Modified: Sat, 28 May 2022 00:51:02 GMT  
		Size: 51.7 MB (51703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fe12babf16ad61003af3e401f503375debf9090b06ef2bb8b467eabc19081b`  
		Last Modified: Sat, 28 May 2022 00:52:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
