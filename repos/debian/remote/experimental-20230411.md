## `debian:experimental-20230411`

```console
$ docker pull debian@sha256:d6793b69ac88e2796d8222fa9df0483696ddfe2a6e96de1701718da3dd93b773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental-20230411` - linux; amd64

```console
$ docker pull debian@sha256:ca7f035edc086e494d9f2050ecc0618b891e379e98f4fdb1e3230a66ad0b672d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc81544d8a3971d7f6f506af29909ede4deeb330da5c293a013edcbabbc6c68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:21:52 GMT
ADD file:eb948b4bfe0963071c224791a81e9295fa552632c5b185f143e3c42c071c4671 in / 
# Wed, 12 Apr 2023 00:21:53 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:277078978190188dc2be36cde72743cfd4b19903cf7c90ceef8421d87590db29`  
		Last Modified: Wed, 12 Apr 2023 00:26:45 GMT  
		Size: 49.3 MB (49287657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24155652d76da641860b0880f1eb77c20820c9755ed8901327813e326271111`  
		Last Modified: Wed, 12 Apr 2023 00:27:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; arm variant v5

```console
$ docker pull debian@sha256:757da19df3991de65047b8f77e388f3741d5b6aa5fc9a384601c6610b48555b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fb7fec78198c8754b5034a59b8db0528f8ba8b9dc39500ab67d68734f93bd8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:49:30 GMT
ADD file:c7802798194547a5f8f88b2a4c08f8c52cecd12552604376c5c392eb22344ac2 in / 
# Wed, 12 Apr 2023 00:49:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:49:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c4f61e47bcde9d351c2b1ecce3b46ee1089df8055f07f42ed9a181bc7afa868b`  
		Last Modified: Wed, 12 Apr 2023 00:53:06 GMT  
		Size: 48.1 MB (48109675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d15a866a52d3a13e07c0423264a8249661d2e640f8fca6e0d82daa3bba3c1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; arm variant v7

```console
$ docker pull debian@sha256:457923685976ee8c6aaf6bc51b5eba2513f7b372cf1813dfc66f7a2d42d3f5cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45890459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ef959bc2bb82aa080821852f23fc9669fd3daa05a2aa8c61afe1b7eca65041`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:29 GMT
ADD file:a85f9bd069b317fe04f7b0e5e2a6e54a4a94ed304e2487154c520f160f81634f in / 
# Wed, 12 Apr 2023 00:01:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:01:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:54d799b49c2235300dac823b010337407851814391945952bc9cbe2adfc39d3c`  
		Last Modified: Wed, 12 Apr 2023 00:06:16 GMT  
		Size: 45.9 MB (45890238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f266b9874326d8744696ecb20f43c6a235ce3e66b7ddfb6a034f15e3737e4f`  
		Last Modified: Wed, 12 Apr 2023 00:06:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d415cb25dd12c62a6508d76376c8fbc554a296f6e0a647b52d6b91ef8076caac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49327883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8ed813437ccdf05e7114285d3c8e2935ed2aa0b9ce9cc9612e32a93ab4a61b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:59 GMT
ADD file:eed6ca617d18b91908df79e437985b8da5417ffb4eb0c52b6cec20e46c00414a in / 
# Wed, 12 Apr 2023 00:41:00 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:41:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9a890b97e54717f3d2b342929339a71068f93c352460bf767e21a39e90688b79`  
		Last Modified: Wed, 12 Apr 2023 00:45:24 GMT  
		Size: 49.3 MB (49327659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de767cde562b4096331329cc56b1ce0017441c9715bfb559abd67ebcff8fde6`  
		Last Modified: Wed, 12 Apr 2023 00:45:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; 386

```console
$ docker pull debian@sha256:160d086cc268d5f0b0c5707abcc7cebea514795e49b3e474185936248551f429
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c073ae6fbf54de0a5f467386fdbc065e18bb2cd1fc6d6ea85a2d3456e8d80f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:50 GMT
ADD file:846fb6727047101baf611eb5e752306b9f0d603546da67314cb4ef21e2f1f54e in / 
# Wed, 12 Apr 2023 00:40:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:41:02 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:308acd63a4eaf4bc5f65e274ce996d9cdbcd66aa3e1fce97faf327125eb14e0a`  
		Last Modified: Wed, 12 Apr 2023 00:46:12 GMT  
		Size: 50.3 MB (50310902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e20b6832994573bc5e69363c770a8098c7bb965b3c6dc74989bd928810991c`  
		Last Modified: Wed, 12 Apr 2023 00:46:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; mips64le

```console
$ docker pull debian@sha256:21f20e067b8c031a8411cefeb6dbaee8ebc2ee5bef352928e7404e0afb99907a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49296474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57b62d7b0bc81496cd6c4f650b7976e091f9170838b072b848d4ead104337c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:13:36 GMT
ADD file:7175a1b08b8243bc539cc1f758d85ccbe24afbc3df6a1f629c7a43839aee5f62 in / 
# Wed, 12 Apr 2023 00:13:41 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:14:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:589b4c3c9d360e937d4513f3ec8af4982019090cf0f68fb06e1e275c06591a76`  
		Last Modified: Wed, 12 Apr 2023 00:21:40 GMT  
		Size: 49.3 MB (49296251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e8aaafc25e00fed4f728c0664478dccdcf9f43ed1708ea8ccbe0fbaed2a1bb`  
		Last Modified: Wed, 12 Apr 2023 00:22:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; ppc64le

```console
$ docker pull debian@sha256:1ee69d64a8be19f5bd1e06a74ffc9cf2726fbd4a286c70863f13a57e58b18b88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53291933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c76d7554eabcbe88b5cedc818303dc922fb264b836768deef356515d8d2da76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:38 GMT
ADD file:930aae2ab6be5d8295a31bf5dd91eee5ee4fa92a08b6159f55cdc6d3bd182e67 in / 
# Wed, 12 Apr 2023 00:10:41 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:10:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4e67fd8b6f31e9a06c3401edfed958df31a0ae78d0692baa41a3d87074423b51`  
		Last Modified: Wed, 12 Apr 2023 00:15:52 GMT  
		Size: 53.3 MB (53291712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27112dd79fe0a748333ffc777c2b7353783f06d8bae54c98d2cfa0f7eb90dd40`  
		Last Modified: Wed, 12 Apr 2023 00:16:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; riscv64

```console
$ docker pull debian@sha256:848f36bcdc59386757ea640d87b9543b0b0e6974b24753e43c9d62a92cfe49a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003a05cc9ec6850682d28a3624bb3de33c33df72a821c873287809c8e36a4c8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:30 GMT
ADD file:f48330c22d0ecd502b8b46026eeef4081864a8a585160caae93e5700a6524a58 in / 
# Wed, 12 Apr 2023 00:10:32 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:11:18 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1b037784414a5f8d993a1f29169b41dbec924bf914e4e324fdd3209ce4445a32`  
		Last Modified: Wed, 12 Apr 2023 00:13:57 GMT  
		Size: 45.5 MB (45494945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91927993230d3dd4786ac01888e74b7a400d90f94093954b120def27101a238d`  
		Last Modified: Wed, 12 Apr 2023 00:14:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230411` - linux; s390x

```console
$ docker pull debian@sha256:9bb2165075db3a6509a9447f86beafeac8f7ba75202b764da22b505ec16b170a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47665290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0a7b534b879a5d04f757626e6f6acf5a4dad5380f6c29124d4cce3940a4ccb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:03:33 GMT
ADD file:9280167c5f0a6008baa6e9d84a780823b1cf741a9935a60531fb30279a421a97 in / 
# Wed, 12 Apr 2023 00:03:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:03:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:967d5de3f09581dfdc9be32037966130e96015074ba7d995ffb521bcb496aedb`  
		Last Modified: Wed, 12 Apr 2023 00:06:36 GMT  
		Size: 47.7 MB (47665070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d61ec497f5f76e5e6a2d2a829e93a2e43b9ad2cbc9586ab0729461604adb3c`  
		Last Modified: Wed, 12 Apr 2023 00:06:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
