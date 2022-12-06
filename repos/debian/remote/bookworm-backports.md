## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:1dd1adbc5ed5b535c4e28895287a76727cd6a59f42cd2468640bbd1053863938
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
$ docker pull debian@sha256:875d73cbf7c491a75587ec5daf871f00153f6cd573f451aedc82817993197f64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50260743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26ce6b066086a8a3c233555e901746ef4e1e14071278b098d00421194331b2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:17 GMT
ADD file:bc800ccc3502eee52ab13da7e930beeea45bff7ec8e6f625f2958550a0e0c4a0 in / 
# Tue, 06 Dec 2022 01:20:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:20:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d5213c1b98149df5de6014f7a0822d3f7c1239b55b191918b5019861d2385bf`  
		Last Modified: Tue, 06 Dec 2022 01:24:15 GMT  
		Size: 50.3 MB (50260519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52174568cd600885e30ce9c4862c1cc3a5e424dd78eaaaf9b9499193b336ce00`  
		Last Modified: Tue, 06 Dec 2022 01:24:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d19933b0abfe66cea4d8192e1cb52793959924e5ffc73ebd4fd8191b126c11ef
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49266067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab808975807d0291b34f6f1d2ee16f008a579ade0e758db9ea73773d8e849eea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:48:32 GMT
ADD file:f5954c36a3601d3dcf67f8701fe7691c7a94bc36e88827c06ff7338a52d56c5f in / 
# Tue, 15 Nov 2022 01:48:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:48:41 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:34757784ba8ccecfd4a2f549aff99cd98b7b291a61176def51827463bc77aa00`  
		Last Modified: Tue, 15 Nov 2022 01:53:14 GMT  
		Size: 49.3 MB (49265841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea519cc0b59c9066fa22011a55ccba82a76d2c001b7a3197cb5075203b23ce7b`  
		Last Modified: Tue, 15 Nov 2022 01:53:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:38c95e0c194a30248700c5745c181e556238f925f18f1320d36f8bf9b7e7a5bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47047317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6622b3cfc990527797ef4e2a9d994463662ef3953deec3bf514625b77ba84c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:57:56 GMT
ADD file:82dd62a6df63f711bc714098f18b9106a7507772b5320c66a30f7ccba2ae24a0 in / 
# Tue, 06 Dec 2022 00:57:57 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 00:58:04 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e675a2bd8a737d1b09b68b33be3a9ae4bf0f69f7b1ce279fd4c63e38d294b1b`  
		Last Modified: Tue, 06 Dec 2022 01:04:50 GMT  
		Size: 47.0 MB (47047090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b88e857f7530a93d2fc07e7656706e14a10a1b28d141df6696152c2cb97da5`  
		Last Modified: Tue, 06 Dec 2022 01:05:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e951862d473047c48d017b0ae02f5eb35605eeb4a0def138f806da72db475593
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50353528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbc8169cb56aca1a37d497c3c09d7da99279f169bdf0029b96500f48373cd68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:57 GMT
ADD file:c622ea356e69bcfb00a0066c22b326eaa514f83ce688202c38b1cdf4e279f65f in / 
# Tue, 15 Nov 2022 01:40:58 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d350c5c763d25fc284c82bdb22268efbb6376d35695fb6f09eef45b2f3dcbd9b`  
		Last Modified: Tue, 15 Nov 2022 01:43:42 GMT  
		Size: 50.4 MB (50353304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a388718881ba9fdb3ed61a5bc422ae96694aebd9c4fe52266f0b0d509a63953`  
		Last Modified: Tue, 15 Nov 2022 01:43:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:6a90bd4ebbe191dca8388c2c114cc5cf413398f06884296bcbd189afcb0e6c79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51345132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c4231895aba98ce8b59552dd0dc7dd1699438dccba8d7726434e7e8113000a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:45 GMT
ADD file:dc52b19235f576e4601a85df40bbca1bd78982afc56d272746728294ee8a335a in / 
# Tue, 15 Nov 2022 01:40:46 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eed5d6b8bc9dedab6a360f9b58991756d109919cc4cac0c030d7c94377a3a13d`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 51.3 MB (51344908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042ca96def17973d32b5e2b3a467cf6e688bb5f1d614258f9526919dc7cece1`  
		Last Modified: Tue, 15 Nov 2022 01:46:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7fcca122167406affb875a8e121e46b758a58d523fc4cd9fe8aba2466e298e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca2b797374b17a6ce039f24729828882fbe793c1321a9b2849615536da93e51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:11:59 GMT
ADD file:0d439a2fdede63b0646f17fe0578b4ebab24012a35c93e6e63e5c511ccce8fe7 in / 
# Tue, 15 Nov 2022 04:12:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:12:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:52449a481885eb7aca2b2fbb088c8d233a6249a8aaaf65e32f8c268ad8340850`  
		Last Modified: Tue, 15 Nov 2022 04:19:19 GMT  
		Size: 50.3 MB (50314192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a83df67b53f6a81ed173410e1f2ce307db48458c0fb0dabbc9cbb599bb161d5`  
		Last Modified: Tue, 15 Nov 2022 04:19:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:42c97ceee5752649009b441a9847323cd40a06b29a932332ca24b97973dcbde7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54319516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5dbde1a1375c815d3bbd9bf8bc9f725f34f52bf63c191e59cfc5363e9ebf0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:16:54 GMT
ADD file:394004d3191138471ba2dd50891718f9142a137ec9018f4f69a653139a98abf1 in / 
# Tue, 06 Dec 2022 01:16:57 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:17:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c1206773e59171c1200c3692244202cc0da97f8fc41cb86ed64f742f1e75b47f`  
		Last Modified: Tue, 06 Dec 2022 01:22:51 GMT  
		Size: 54.3 MB (54319290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe4173c0e797dc3324051f241bd58a315afae24c4c6afb993f92636cd546495`  
		Last Modified: Tue, 06 Dec 2022 01:23:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:0c3a1a5f833504dc9a0e6f4e56b738ab7d0c1f618d69a14cb3a5bd64ee7eee83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48707625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8502835a8a992a5a6871006cad7480ba1206d6f8d158e0c902e2945609cb2274`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:40 GMT
ADD file:c4f7dc2db7bd88fefb0d92414f2efb03e7ea14cb79f11eb857199ab31069aaa7 in / 
# Tue, 15 Nov 2022 01:41:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:10619af8bae5734a158de8dfe5f8646bf40e3e004bd7a3c4ee4a89da0bbb688f`  
		Last Modified: Tue, 15 Nov 2022 01:46:45 GMT  
		Size: 48.7 MB (48707400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccd150a00af4476d2960dafbf99256d4def4b1e6cecb1fccae644ca413197c`  
		Last Modified: Tue, 15 Nov 2022 01:46:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
