## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:4d7181d4dfa073dacb0bfcdccfe00877f8552afdc847b0c98202f126b67c73c0
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
$ docker pull debian@sha256:ef7812a599a58c346d949028ad5742a121bc4d6316aa745293a3e8d448eb85c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55055528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806d590d2f5b342480c8f6ab41e7cf886ad37bd0fd8cd90e5500cddec69edb1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:25 GMT
ADD file:aa8ed94ddb59e4c0538b39dcaa7040aa0aa62297242af9074715df5e49310d5c in / 
# Tue, 04 Jul 2023 01:21:25 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:21:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:70705a13f194adda8510677de1e9a79a43350123f9bd3d7a7be637b9f7084f32`  
		Last Modified: Tue, 04 Jul 2023 01:27:13 GMT  
		Size: 55.1 MB (55055303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66222735b3343b5b6b4d785e66b8f874dfb990b0f598d08cd3081d54660f5b4`  
		Last Modified: Tue, 04 Jul 2023 01:27:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a1c142aaf6010ed412209a6930b30a61454d97e222e475d389c7c11cf3339218
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231655e7e94dd41818c717cf6ad97fade4aa67795febe1247db0de2e781766a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:55 GMT
ADD file:eedd41901674350e1e1469ed0910b376f827555b17b22e3e10f0110f86d62478 in / 
# Tue, 04 Jul 2023 00:48:56 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:48:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d4e822f3c7ca5566f101f8d90ca82f6f749f73c7518367686a1e48cb3d17f459`  
		Last Modified: Tue, 04 Jul 2023 00:52:58 GMT  
		Size: 52.6 MB (52556780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7a7789c97a6d50342a32a55eb69b34d57a5a9e65f9dba2787d9b6a7f76d30`  
		Last Modified: Tue, 04 Jul 2023 00:53:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:aef5318ba503c33f45cf7a269cfb2e6f670e8175c9b00b0a8f6e16192b2893f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50218493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155602c72582ddb6094901a521ba97c5577a41c962da17679d86d43c4009170c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:59:22 GMT
ADD file:ea176a714b2523843bef5db3cdb0b649af02c3656e86f8c2c4f18054fae67225 in / 
# Tue, 04 Jul 2023 00:59:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:59:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:172a14bdbe7b3b2f83f795e8c55945aea2def70aa907d371cb1f32a71323d65f`  
		Last Modified: Tue, 04 Jul 2023 01:05:08 GMT  
		Size: 50.2 MB (50218268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7c97b4dfbcb704327b6bfaae85ad8b672d6a7846f992b10fb34ce524a5699`  
		Last Modified: Tue, 04 Jul 2023 01:05:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f90f6daecb83d31f33666d2e1103cc71189bdf79526e3111f59afed609772170
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53704202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c28916dd4ff432e265cbd6c76ba0d705b54f34c9176869bf0e59d96de13d70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:33 GMT
ADD file:1a5822a96f77d75084868721a1bb8d1591dfd1cd3dc5db29e59956edafa16bdb in / 
# Tue, 04 Jul 2023 01:58:33 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:58:36 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3311ddc370e1bf7a67ee3323c736fc8d88636bb086836df8086317ecae682df2`  
		Last Modified: Tue, 04 Jul 2023 02:03:28 GMT  
		Size: 53.7 MB (53703976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8048f09539baa115a9c083cc28085c52b8d868967b6db83c8c02f71144f3ffcb`  
		Last Modified: Tue, 04 Jul 2023 02:03:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:2592e2bc10273173f750e0ca7dfe48506731d33afd0a5782f7321aad3d819131
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4e855f5baba675db26cfb1611d146ebcaac1f8248b52f9c80bc7df20f20f73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:57 GMT
ADD file:57c69bd29985e87430db91f2af1d239154249b5574a15b60df18114148c5bc16 in / 
# Tue, 04 Jul 2023 01:39:58 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:40:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7367da3b7b4ed975852a58cda403c7be1fb59785e1b07d9f0b3fe0d635117474`  
		Last Modified: Tue, 04 Jul 2023 01:45:54 GMT  
		Size: 56.0 MB (56040748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955341ee1324c1f341f307c46792810a457fd7e5af2c43553de2c2cbbb1263d6`  
		Last Modified: Tue, 04 Jul 2023 01:46:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9ed26dd86c73f492bb27b64317b40d92601467eb7c592295eec86d7fd8ed7415
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f509d0d0fe4f01b734f2050b452568f8f751d5648994bae95967965f76ef932`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:11:17 GMT
ADD file:01e73873458ff017b9060e02c6c6d6e80dd596c5d69932be1af564907154c729 in / 
# Tue, 04 Jul 2023 01:11:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:11:36 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cad33424acd55ddf10c5c761d89e4e342d970ebf80cbd441dafc9c4afaf0224b`  
		Last Modified: Tue, 04 Jul 2023 01:22:03 GMT  
		Size: 53.3 MB (53270477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce2a6c04567e0c79f2b48c9c4f3d13c777db985e3eae22f07a9289af88866c`  
		Last Modified: Tue, 04 Jul 2023 01:22:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6a99017a0a473945817202052d513e7e2dbf48ca1a272e1bffebf7c58e0e9e0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58927961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1046574891621967c2362700f745937d96160d35c2e556689e72c42e0c71bf59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:53 GMT
ADD file:28017068c8ae84b6dadb06a194af584a65f0ea1966327d6ee4c66ff6b29bc8cf in / 
# Tue, 04 Jul 2023 01:18:56 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:19:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4a92e1f73b9a25672e5117ddfc8a47ace827a65a17ac563c3cef3151fe2f94cd`  
		Last Modified: Tue, 04 Jul 2023 01:26:10 GMT  
		Size: 58.9 MB (58927737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0704b61031f4c425841aebeb50cbdc2e0e681d3c24fdf2488782cb58109308`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:f1728a784f67ec26b605733b559378140df26d2a7c08442ecc83807b6368a995
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53288396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a838f2edc5fe106d82241bc217d282e0e3e0d5e519432d9afc79c4b1949b883`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:56 GMT
ADD file:9a5b565563f2ef29c23b2ae9528258400fa561c8621431baa41e5586c4481a8b in / 
# Tue, 04 Jul 2023 01:33:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:33:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fe6dd3e95702ff7fd336d8943229a96a472888c11decf348b3344b315fb5a372`  
		Last Modified: Tue, 04 Jul 2023 01:37:50 GMT  
		Size: 53.3 MB (53288169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac660a6995d12b63b75062ad31a1aa3ea2639ae2c8dbd213107840d67e2390b`  
		Last Modified: Tue, 04 Jul 2023 01:37:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
