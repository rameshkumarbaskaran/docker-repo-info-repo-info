## `debian:trixie-backports`

```console
$ docker pull debian@sha256:353db64a0662fa98e11baa69b2d68031e61a2a6f12359581284dcf01e92e79e4
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:5ae29e839124df52a631357d8e4ea09cdc75337a2176ee0a98be9cde2a7eec5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeec5e1575d2be00f72da3684ea61c06a1afef0a097e7287bae17d898b551b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:23:01 GMT
ADD file:69ddb6bf8a54cc4c13fa6dfc75c953d997384f31131296eba0fe4670ab3281bb in / 
# Tue, 04 Jul 2023 01:23:02 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:23:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7b026d231b019b0ddfd89687759b2889cdfa3c816e7bb7bff4316db584f02cb3`  
		Last Modified: Tue, 04 Jul 2023 01:29:17 GMT  
		Size: 49.5 MB (49523846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc46b360b0a56bc5e5d179eaa095c07bd7d2e02b033040aada5a6699db028794`  
		Last Modified: Tue, 04 Jul 2023 01:29:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e81d3682081739607a458f874cdf09e6f82488329bbc3adb6658669b11e1b2da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47360291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae32a37a97d059a474f4b4c1bfb7aed1b42298cbc7ec86161fa6fe78f69b4e75`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:49:59 GMT
ADD file:0ffd95af69945bc7c3ba2733bffd453f61419b678dcc1b0bf13261d9a2d147f7 in / 
# Tue, 04 Jul 2023 00:49:59 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:50:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:059b0228783b958bcd75527dc7506c02509e9b3a009b9e7f5b944545d6d86929`  
		Last Modified: Tue, 04 Jul 2023 00:55:11 GMT  
		Size: 47.4 MB (47360068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800e40cbc2bdb55b4e850e1de91b839cf32b2fe10878fa6e6bfb56e2245fb5e6`  
		Last Modified: Tue, 04 Jul 2023 00:55:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:470115159880b4f4ae66a971819f3fd22f86f726a586d6732ce135e980bcedb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45183044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10edec909c5814fbc1eec58d5f35fc76c37103c447f59b87481bce5752a709c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:00:59 GMT
ADD file:d1d870c89e7d21b3459cde2dabaf0d8fbc038324334dfb59648191201c0881a6 in / 
# Tue, 04 Jul 2023 01:00:59 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:01:03 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de599662316fbbb0e5a107c34fc84f0bd6cce1eae2febdee5f9a166bcbe6f898`  
		Last Modified: Tue, 04 Jul 2023 01:07:24 GMT  
		Size: 45.2 MB (45182820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5670106917a9946afac9ad64e88b57f1d74426abd2e7fb9c5a1690541d0674ac`  
		Last Modified: Tue, 04 Jul 2023 01:07:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8bbc37cb7755b44e0509a294e381749150c8afb18b22dffbb49c4ca0b5edb55c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab30828c59efc7b5b188a8fad2f79d62a74b226ca2d3bce5339f16d9db71104b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:59:36 GMT
ADD file:e83c96cb391bb6f4a4236baff0c8be47ff4ea09826f95481497333dddc3537ea in / 
# Tue, 04 Jul 2023 01:59:37 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:59:40 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d728e68b504cba85127d7d3e5493d24223ae3af314b4e73d6b74bdebf7911f05`  
		Last Modified: Tue, 04 Jul 2023 02:05:27 GMT  
		Size: 49.5 MB (49524491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96724154c094afab3d9be4ffa4d0084c788c6cd10f3a427b919a6360ae610c3`  
		Last Modified: Tue, 04 Jul 2023 02:05:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:ba31134ada6ef14473e8ed19d30d2657df5a50fc7558e867adc9a70a5e6f3839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50539630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e660080e5694a4f09be0f2e019e3364036d887965eb04fae883db78dadfed872`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:41:27 GMT
ADD file:034bf0762755f9dc5cb0cea6768f68025634eda8045c112ef95777d21df6ecf3 in / 
# Tue, 04 Jul 2023 01:41:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:efb3d19d1083945d3c3a14221887db9fd1e087f333da06937d0ec9bfe0c79e18`  
		Last Modified: Tue, 04 Jul 2023 01:48:17 GMT  
		Size: 50.5 MB (50539409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc339673cb7adea6360b02bf6a64935dc01ab1ea025daf75d817586e45465d0`  
		Last Modified: Tue, 04 Jul 2023 01:48:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a5b9a3e900baa05439aaca266817d49d7ff2da69cab32b9b6e05e3bb435a6251
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49497212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0c7887109ce3a92d8c3fa5cfb0a7fdb7cdb5d775ec6594b947811d036b2aa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:15:54 GMT
ADD file:ae6c6291352d35c9053a1b89fa15bd2eb76add307e5059d83474f17b2e138b31 in / 
# Tue, 04 Jul 2023 01:15:59 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:16:13 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:67e71ca2fad81efa04d26e36aee19d65985a3b0a387729559324ca4e38246677`  
		Last Modified: Tue, 04 Jul 2023 01:26:47 GMT  
		Size: 49.5 MB (49496987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ca92ca112ca9ef44793598b225b1d8646aa78347045e9ae71982e45ed5ea9`  
		Last Modified: Tue, 04 Jul 2023 01:26:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a33f752d2bf7e0e56ca0059f5010413456e67f9e27a6c058a35e68f3e38ea350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53510703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03510c953e92fe5f5f7609533f15debefd498f7491ebeea3b4091a1d5c8ee12`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:33 GMT
ADD file:0ceaf5be903c5d350c3e3aa5ba446b3e6ef07b387c44d4fcfe5a4ff0d3c9dafc in / 
# Tue, 04 Jul 2023 01:21:38 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:21:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a29695f02132f5ced01dc6d2db95e88b5cc475771c1b689b45229c55d07594e`  
		Last Modified: Tue, 04 Jul 2023 01:29:35 GMT  
		Size: 53.5 MB (53510478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33912edaabc2ceaaa6173c2a26b4a9a7c5b4909ab28efc7a2402629e6c04f4c`  
		Last Modified: Tue, 04 Jul 2023 01:29:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:05c18702c98eebf3d9503da696dec797788964b51a836f2d5fc507d1849e9525
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47950007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d6457b344c1d4ed9feaf5f9feba7c6039b6f3748942082d8cfd44f81f80689`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:34:52 GMT
ADD file:9ec04d3ce271a93cb5627cb0001517d58e07016d24e0e80cbdcb8bda54e69f8d in / 
# Tue, 04 Jul 2023 01:34:55 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:35:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:56cf8724500ec05fe7063f36d4625803ce264bb1a82d2faaabba9d1be0008b8b`  
		Last Modified: Tue, 04 Jul 2023 01:39:27 GMT  
		Size: 47.9 MB (47949785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da86eb9d735bfc2a334b19d19061c3401d6c7b1bb8369c5e07768ba511ae4b4f`  
		Last Modified: Tue, 04 Jul 2023 01:39:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
