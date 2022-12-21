## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:514c4903ed958ff0b452fa3bee150b22e0f0e090628e66d38c6ff6869778a7c0
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:0445b366d7ec0d457e1aa3307e6b38272e5179ed234e6693c9a3108a69bb74c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75455b18dc011b515e8033d25ddef5a258fc537b6f2424001df0b0acb890b89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:01 GMT
ADD file:5498bb69da6f2fdd15556904d80120042d5bb48f73fc9f20a2d1bd5a908e0017 in / 
# Wed, 21 Dec 2022 01:20:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:20:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2eed4289b3de645a7af9bc81fe7c50d50a1c7aae044a61e100a676b9e6224267`  
		Last Modified: Wed, 21 Dec 2022 01:23:37 GMT  
		Size: 50.3 MB (50324468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1d3835c88afe761e9763b62614587c46628d4d902ec9e45d98591161f2367a`  
		Last Modified: Wed, 21 Dec 2022 01:23:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:eb691f7467451bb8eb4cef4d3c4e47a931cc840a0afa7ce4bb2f59a6f09a4f02
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0796435fedd15358a0d625d05eceecff2781a325ab53b0fed3d44b366cb73f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:28 GMT
ADD file:1a47719ac251c6eab2626d584c016fd54fb5ad1212453da6f254e2977d844ec9 in / 
# Wed, 21 Dec 2022 01:48:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:48:35 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5a2ba72506fbd85b58dc5575f5616efa7992eac16768aa35e10922a41b5bc83a`  
		Last Modified: Wed, 21 Dec 2022 01:52:47 GMT  
		Size: 49.3 MB (49285345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c0419b047fcf453e7e56322606c0a0293b211fb4dedcdefaa5afb6e92cb8`  
		Last Modified: Wed, 21 Dec 2022 01:52:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b03927b110dbad97a584357814c8670b0646af18781b25f63e02d772725f4910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47101485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95a800130fff61076199f4baf93286e6118ff016ef62a349c64e9cd2a7e8570`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:57:40 GMT
ADD file:3a39343b0809f063616f72499663466e4a509b48e03fab9262c152a211f015f7 in / 
# Wed, 21 Dec 2022 01:57:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:57:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d2b0b92caaf35a430a2b891b3ae1c59a6cf60477263bd8e7a30cda427435d63`  
		Last Modified: Wed, 21 Dec 2022 02:03:55 GMT  
		Size: 47.1 MB (47101260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a447029573a0f4911e2d0414cf674386094a2eac72379823387ce9b9784131`  
		Last Modified: Wed, 21 Dec 2022 02:04:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f7212830163caecb653b9a474357930a14e4ba30a5a0310592e8e4c072e8846c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50373068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4776657acec18251ce40d737ea96539d8274d444944c93c696bd7bb3fbec4d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:25 GMT
ADD file:b83d427ad5bc07aecb363a59c19809d66f1425c1d8df7a4d66eb56624cf5fcf3 in / 
# Wed, 21 Dec 2022 01:39:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:39:29 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be520eae96ff7c486efeba591ba872089e3b618ce226d23bf2b72f07277fb6fc`  
		Last Modified: Wed, 21 Dec 2022 01:42:15 GMT  
		Size: 50.4 MB (50372842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b0da8c5a600ec1ec7d1e097aa0640616fd6e078aba530c403dc5378565f57b`  
		Last Modified: Wed, 21 Dec 2022 01:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:dddee91f5768082d8b9991aef753a6775118402c72dd0cadba99ce56b1096ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddc514403d1ee0f60f512ef84a53d4fb8cbddc5032db640236d0b6a8301ee28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:38:43 GMT
ADD file:f11f9a6e73a1ba42c97eb037cc53f119df6d6b050eaeb10df2ae716f4eabd8bf in / 
# Wed, 21 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:38:50 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bce8ae6c08a69b30b85b1e939b782fc4dee31791e21ed3abbf56d1ec1dde0381`  
		Last Modified: Wed, 21 Dec 2022 01:43:40 GMT  
		Size: 51.4 MB (51363529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642ad288a689395e944ddb0884c626d2a920b2e25769692ed209a16ee5884e62`  
		Last Modified: Wed, 21 Dec 2022 01:43:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f91715cf01aa1d7f1628caddaf4db50c48e0be8aea4a531c0173d30add8079d9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50336974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4fabd5e9d86299c96c9ac3091d77a5ecfcc7d65a65ff7fd8b29f045d5ae0b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:08:43 GMT
ADD file:b2458569ae73892acee2eab6d63bd5fac233b8f2939355fc7605c8906c1bbd30 in / 
# Wed, 21 Dec 2022 01:08:49 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:08:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:63a99937a40bd4c10c6b0d4be0826a18d963fdd5ca9c794853e98ca819d68691`  
		Last Modified: Wed, 21 Dec 2022 01:16:43 GMT  
		Size: 50.3 MB (50336746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d129eb990c579f00619b717b3bd5a5d11e01e6b1517e507c672a24aa6a64ab9`  
		Last Modified: Wed, 21 Dec 2022 01:16:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2c292d3815d7c2a64edf80094603daa2127deab04d7d095aa18e8b4beb611964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54374050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4858a17369cb0fdc49cfa1bd57c25e43552a040eefc736ef220c084f003e6e97`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:16:40 GMT
ADD file:ddf53eeecd4e99f9ac6dd446b84eed33212dae1b2a9476907b99dc988c316e5e in / 
# Wed, 21 Dec 2022 01:16:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:16:52 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9a50dadcc8beda7926088df1652aba274c8cf1817cd6956a9342f3b25db470e6`  
		Last Modified: Wed, 21 Dec 2022 01:21:57 GMT  
		Size: 54.4 MB (54373822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafe0cefc253c2a47e3ab3d7dfcceee7b73c5ffb4ee1c2294eeac56c5c147ed8`  
		Last Modified: Wed, 21 Dec 2022 01:22:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:1933f27a19371949a656de3a06e7ac69dc1d57017b73fe29faca47e1a0440d99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48719688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3596a4044a0be59cec567317da59d6793dbe0e309a1921445fc9ebeb1c73e622`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:58 GMT
ADD file:607007f7678c66cb1975d361bd26444fe0903e3a9dd7050476438a65264973e4 in / 
# Wed, 21 Dec 2022 01:42:08 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ac168fec9b2e04c14130a8666b154d956cef535df9b833dd775de5aa941079f`  
		Last Modified: Wed, 21 Dec 2022 01:48:22 GMT  
		Size: 48.7 MB (48719460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513360853618fc5ffb4f30302f9ca3dca1d9c5f79d86b449bb3eade889d70f2`  
		Last Modified: Wed, 21 Dec 2022 01:48:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
