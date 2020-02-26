## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:798d7400deb3e8f02fc75674eced03ce08a7c9762bba4b1ee63f3571d88dfe5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:5c5862fb4a28b49b47cba4c54131e898d8eba9089ecf7fdfd3f77d34149ae13f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51852964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2483e30fc0fa1be2715ef7a668b25b60447030a14f6579f804d828cd77df7991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:36:28 GMT
ADD file:7d01effeba890adb1756ba0a76c42c1dde5a189003943fbf4cb9fae0c0e1a046 in / 
# Wed, 26 Feb 2020 00:36:28 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:36:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7a4501da464e996edc2ef85325afe9881a58061a9a35b142ca7f0ba598553e49`  
		Last Modified: Wed, 26 Feb 2020 00:43:35 GMT  
		Size: 51.9 MB (51852739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04d80762c9ed15fb383287c1442115b6da6cddddd14ea1d10a36ea0cec8f26b`  
		Last Modified: Wed, 26 Feb 2020 00:43:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:22cafd56302521ccc051266b36672b0c8dfa1fdce0a71340aa46e80df939c2e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49859657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ff02b243e07f95575e057650c05e61bda9d5cf619255bf0627dd24efc6df5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:25 GMT
ADD file:cd3f4cae9b31b83faef159941db546ad620281a9de9ad8b4c2e2230e329f629c in / 
# Wed, 26 Feb 2020 00:46:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:46:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b5f1b944f6f81b9832613484a0ab69b94fc4d7e69cec7cf9246276a84f198955`  
		Last Modified: Wed, 26 Feb 2020 00:58:09 GMT  
		Size: 49.9 MB (49859431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ba68e62c2e064864fdd7198522e9f4737c0c3a69edd34c45d91bf1176306d9`  
		Last Modified: Wed, 26 Feb 2020 00:58:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d6fee4ed9d69ee7055a79e034cd35af6ea767c232d135198dd55d21c6d46de93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47581516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b252715f4f7a7c3caef2fa6951386657c2c030c64fb337b245cd590da66d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:49:40 GMT
ADD file:516c2d0189c8132f97d954209787ec2c833e16a9d8a4056cc9ed22510c721b48 in / 
# Wed, 26 Feb 2020 00:49:43 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:49:52 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d46b4a12bd08cdd498cc190f7d350b7bfa151e105942f36a185990c238f53695`  
		Last Modified: Wed, 26 Feb 2020 01:06:24 GMT  
		Size: 47.6 MB (47581289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3662a35f2cb4cd59423be4e18940240ba91121777bde480055e8e04c4c86ea7e`  
		Last Modified: Wed, 26 Feb 2020 01:06:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6327e02bbaf2fff6979fe3fcd6f1a24ed8078ff08eb465f6e95f5a6988f62299
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50808778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725d8845ad261bbc4f9f4db5c14088da374d59b0d5c1e084d3173cbecf81a36c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:45:20 GMT
ADD file:6771f02669c2a4d080cd86fa10f39851d26351e4a29f9ff3d63a76e1865f96ad in / 
# Wed, 26 Feb 2020 00:45:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:45:31 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f822750796cfd016baf6c8125f67a171683174c26da351c46b78a6cc9d234372`  
		Last Modified: Wed, 26 Feb 2020 00:55:10 GMT  
		Size: 50.8 MB (50808549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24135e67773075353d8fd3162feebd949b5dd308011136985f6029e9d18c28eb`  
		Last Modified: Wed, 26 Feb 2020 00:55:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:c5e71c2a0be1b3863870a767ba468a8f62205991e91d9540c04205df08690c90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53002885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf92564260f1fac699183a3b9761a2be70654f4fb7bdb100f32a492cf184df7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:31:20 GMT
ADD file:d6037ec8e49283f4a0fd36cfd0bc4723725164526c4c56459e4c9f3d73c61d06 in / 
# Wed, 26 Feb 2020 00:31:20 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:31:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d581a0f5f74a9924d3ed374e49a0171892551a9eef1c8d7efea523bdb4334da`  
		Last Modified: Wed, 26 Feb 2020 00:37:37 GMT  
		Size: 53.0 MB (53002659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339361d51a1eba6a3a8ba5abe7e32189534161794389babfced9166d8b470e6`  
		Last Modified: Wed, 26 Feb 2020 00:37:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:abbe696701d18ee75c436e149ec5bbfcf8ce18c563ee6b17af48094e8ee8e743
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55696830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee5a36ba6fee0351648945a308ddaa0f66999422e674770ec053160b9396af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:27:16 GMT
ADD file:063d213502b9de933570a06d59fc9054327af22f028f43bf3dae3bb2337e65d3 in / 
# Wed, 26 Feb 2020 01:27:23 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:27:41 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61866abd58bd3dfd0faa8b784006b357e3857249b9f14f991b94b177781a85f9`  
		Last Modified: Wed, 26 Feb 2020 01:45:39 GMT  
		Size: 55.7 MB (55696604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c54c62f53e51f7fa38c8d7d117836455ab4ba5b9b41f1a2595279bf2d4eefea`  
		Last Modified: Wed, 26 Feb 2020 01:45:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:ab132c522858c6fda7bda8b69c321426918990e2e245fd9499aba3276d393332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf626562f4ef0b6d9d2d74cad9c67b76528739cbcb135cb64bf36a381922aa3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:50 GMT
ADD file:1f369094a028b147c0bd0497bf726fed9867b40f8ab4ff8cbca77817e313d055 in / 
# Wed, 26 Feb 2020 00:41:58 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:42:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d902b39656b1700fbfc6beb02acedb31fb8f4ec23e536097b114147f2c25b942`  
		Last Modified: Wed, 26 Feb 2020 00:47:01 GMT  
		Size: 50.5 MB (50483632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812f9fd59320720c4398929adb6221fa64e59b3b541b9226e3854abee17ddb72`  
		Last Modified: Wed, 26 Feb 2020 00:47:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
