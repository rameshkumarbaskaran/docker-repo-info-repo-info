## `debian:stable-backports`

```console
$ docker pull debian@sha256:47099e3a2a4ce16b6a50a215409aae5fb5942ac3430839c344c11c836921d769
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
$ docker pull debian@sha256:fe191261248867971848f3bb51dc5b384ed4a7b9eebc56f986f3af490d008f49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55046204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fa63c7a9bce28bd07f0e7b10baac4eb97eae10d3cc001273864df945999ea4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:18 GMT
ADD file:4902855598159d0e8097c7927725e57b89a4bfd7e1793fc0dafdd508a11c4986 in / 
# Wed, 01 Mar 2023 04:11:19 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:11:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f4adb3bdd5c92354e9a5bbb61245c02e97a7f4cb20e49c20844defd9c5cf66ce`  
		Last Modified: Wed, 01 Mar 2023 04:16:25 GMT  
		Size: 55.0 MB (55045981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8bf4fb12ed6deef654e7d2709cae829fc73669de550293e0fd7ec02ab12d4`  
		Last Modified: Wed, 01 Mar 2023 04:16:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:258ca5d9301dae8847c46c645edfbc083bc987d54411a44599a737f9ff24e592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52550083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6bc019945173b3d5ecd9acfa97c8e6108fac84b6cf842130c8232d65bdf06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:16 GMT
ADD file:bad8a3eb985558e32de17b6b7121afc340470d655c3b08489a077f98053cc37f in / 
# Wed, 01 Mar 2023 01:49:16 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:49:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54c6387de315154f0c06420043cbd076f0c142eac6eda8dd70a4d02085792016`  
		Last Modified: Wed, 01 Mar 2023 01:53:54 GMT  
		Size: 52.5 MB (52549861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648dc579297df79872055021b611256fd3578914f40cb6f6559c989cb05edbc8`  
		Last Modified: Wed, 01 Mar 2023 01:54:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:21a3334fcfc5de15f3f8d447869015a287d7cf6b95e2e764df07684957842d87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dedae90b3626ea168959f524d1745db6347f1dbbf1a3a563edb6996734e581`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:53 GMT
ADD file:0bbb7a30608fd2703237856965ffd2844f6b30d88b0c6f59e29ce3cd307724bd in / 
# Wed, 01 Mar 2023 01:58:53 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:58:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ad252180deb3803ff4fa886cc353753ff347b34e8bfcdd293dbf3e459e00d47`  
		Last Modified: Wed, 01 Mar 2023 02:05:25 GMT  
		Size: 50.2 MB (50212037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afffd1eb52dfcd8d0752869842e37a3eec357b79462a5ff91ae6c9439477cf21`  
		Last Modified: Wed, 01 Mar 2023 02:05:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:af5b1a13677dc572a202c915295557ba0a1cc7f36414cdedfba6f2628dae0aca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53703364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6af3ac4b539a67ad49009b0350818704a0074e01984aca3583a88c171532be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:55 GMT
ADD file:3b227c85bf0970aced33c4da102d7d282e814bf53a84d6a6ef7f581bbc76a7bf in / 
# Thu, 23 Mar 2023 00:45:56 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2312bb915b25efe9ce812b12ae65ea209b43c9ef384f3295eb1c663aa11a97b7`  
		Last Modified: Thu, 23 Mar 2023 00:50:01 GMT  
		Size: 53.7 MB (53703140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4208e1943b2bc6d2be32d78fb560f9a2bb957391905222a90db5de8eb285c7`  
		Last Modified: Thu, 23 Mar 2023 00:50:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:f8d4385f76f1996d13c4bbd524c1eb83161f07ee1a4caaa0f336cb87975b4b1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56028068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7f5665d1ac0aa9d2b3a2487d0c704c8646b0ffdd0dce5e76b220c632c58f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:40:31 GMT
ADD file:7e6282db7e6f5f89339f56dff6a7ce78d25479aad91e687d59b76948cd43af7c in / 
# Thu, 23 Mar 2023 00:40:31 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:255456fff76dbf9560f73643299d3b99f21e9ec4f1129ea6904f33328be0add3`  
		Last Modified: Thu, 23 Mar 2023 00:45:26 GMT  
		Size: 56.0 MB (56027847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc4a69a8fc711faca0cd78810adca0d551a9567c69a57f1c28db53991ab21ce`  
		Last Modified: Thu, 23 Mar 2023 00:45:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ce0c024eddce8bc6b7665809bd5b37e5c0f3ad2b60d09bc7fdf9c0dba4b8c307
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53265359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a217b35f825783e2e9c9b60e52a0695692975af5daa78b5f667f979b0cc17d5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:12:31 GMT
ADD file:292d4f2b6a8c55cc444ae52ea2812d03ff2cb0364b433d839cf6eaed1ef271b5 in / 
# Wed, 01 Mar 2023 02:12:36 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:12:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b309c4036eed767322c90d4ba6830bf2e6f25df909b4b9309ce8f0b85efc718c`  
		Last Modified: Wed, 01 Mar 2023 02:20:40 GMT  
		Size: 53.3 MB (53265133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084316f8e187ec49e91333fe55b597a5b4d01a7e24b3c4a5131cd738ada5948b`  
		Last Modified: Wed, 01 Mar 2023 02:20:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:10f7cd17f83bf858c1c80d3e51e79bb62f231556bc6333e90ecd779a2602e5b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58921498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7774771f4d5cc2e4dc705a45b01baa919e8c06b58dda52b443ff190822f311`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:48:33 GMT
ADD file:6e66d6df3e12f245e1d02beb5f0f838b9e40f5ccd5cdcb4f6c5e3a9461f2a3f5 in / 
# Wed, 01 Mar 2023 04:48:37 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:48:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2e550d2bbbbe1ef1a174ed14bdebf17a9a5e786b62dce6f59cef72731bb0045`  
		Last Modified: Wed, 01 Mar 2023 04:55:12 GMT  
		Size: 58.9 MB (58921275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b6d54ebb9025f13a38cd8d6797c99a842dd5bf07976dc6f28550abfed59bfe`  
		Last Modified: Wed, 01 Mar 2023 04:55:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5fd09598a60fea569b4e487566a3c2ce5e7ead38df716e904047db37bc79d33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53277681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c618df44e605abd028560eb9b16c3922bc8be3aebf474b8e0bca911b1e85b822`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:41 GMT
ADD file:0a147643a8506b1b4bccf8b33cb7a3868d9279381b0cd1da59e01d3eb3e3490c in / 
# Thu, 23 Mar 2023 00:44:46 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:44:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5e53e6370cdd67572dcf9ec5a8f5998c3025aff2de4beadf65f001656040863`  
		Last Modified: Thu, 23 Mar 2023 00:47:52 GMT  
		Size: 53.3 MB (53277458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c6dc75bbf8906d791b4ccba1e23ed018394090239d152f8b554f2ffa82a920`  
		Last Modified: Thu, 23 Mar 2023 00:47:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
