## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:5021c2e26f468d1db79bdb0ff675e0c238115f3732a7b46ec9ae522136b08b09
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:f648a0c55eb9d4fd641ecc99d15abb4f0bc015fb27e2ad2a420c006b168c623b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54945845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cfe562feb956d8b99448a87fdff1347370638d6d99b097d8f5ef7c9b4af937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:20:08 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d23b60a02c634028eaec370b83e7d3745882275f7a3337705e729c024004ca4`  
		Last Modified: Wed, 11 May 2022 01:25:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5ac485b588bc028c0c69e3e39750cf7eb0e5e89a250a1946a6a619744d23df86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090dbffd51e5f3ad904264a913616936f4661da704612770b0940654b832bc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:59 GMT
ADD file:b4fea5a360c5cca5abc5866da48126a30eeaf4e976d09c479958fe445dae8021 in / 
# Wed, 11 May 2022 00:49:59 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:50:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ca4fabca59ca0d617061b776745ff41fdc3968ce90dd2b9198717e0bae91d98`  
		Last Modified: Wed, 11 May 2022 01:05:03 GMT  
		Size: 52.5 MB (52476689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a0e22799d830428109d08dacdcac932130ffb23a4797141403570088ddc1ad`  
		Last Modified: Wed, 11 May 2022 01:05:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:23260cd97f5e96239e230d87f7f537d47f056be262486aa99854b03936fa07bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00b31432905a0f49c1ef0dbd12602e9f57bae33c966d1c6914a942c80330bcc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:59:10 GMT
ADD file:faa82773e36b14c218e792730b0264c016864613a8d43cfaa33864075b0ef169 in / 
# Sat, 28 May 2022 00:59:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:59:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8c8b1770c0de8d780b721bb37e9a8b6e5071a83530a584b1aed8ddc9aa12dd00`  
		Last Modified: Sat, 28 May 2022 01:14:50 GMT  
		Size: 50.2 MB (50199379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941021ad14292cd98eb98f258d01ae7d775cdaf17cc2920752091085fa3f72a5`  
		Last Modified: Sat, 28 May 2022 01:15:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5f7bc82ced98407b546208f368eac2ee513475de2244225c1f98d8cdba207efd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53697173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e35e2320e0c615bd7a8b443b7d7949e0d4c486424bc546350b4439c00c705cd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:31 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb0b00d5124a1910331bfe1dd2dcf13c1e434a1254ed813b150fb6b21ca2d2`  
		Last Modified: Sat, 28 May 2022 00:47:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:4cb21866a6e08e9dc239fdb5da9248718cb836599d7b145dcbf601f91425a1a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56008313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05acb7141c5a47e298e2f2167863562932e5c901f02dc01dae789891df31a79`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:16 GMT
ADD file:2ecdc28ede565866b7302862c5e2a4b70a3afb165b383a4df315957be6dd754c in / 
# Sat, 28 May 2022 00:39:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:39:24 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9460ac70d7d688bab5f76bf5c30d1d8577c1fe0b74778427b0febf82ec246360`  
		Last Modified: Sat, 28 May 2022 00:46:11 GMT  
		Size: 56.0 MB (56008088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9b775ef6d45d449dee1714cfddb0827d81b1be37fa281feed250f58497773a`  
		Last Modified: Sat, 28 May 2022 00:46:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9a995b1c25e7c084432dd07c951e013fb582beaca6a246042b59cc67a410af06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53205767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ae758ad55e8cc960b1e3e0991d23323a9381b8b7c4007944f338ef8c80e16e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:22:56 GMT
ADD file:eb055eefa53e1ab6b7358bc8e543f3b7e2016eb48a65d6930cc4b4367b380cfd in / 
# Wed, 11 May 2022 02:23:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:23:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0723f7ee145d9214b27021d88822f2da789ed74e757924ae6c8074085507c2dd`  
		Last Modified: Wed, 11 May 2022 02:33:00 GMT  
		Size: 53.2 MB (53205540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f5f4128694b9c22a03e86af67b8992cff33e54e1a88faee3c5cda6a001f7d6`  
		Last Modified: Wed, 11 May 2022 02:33:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea4114cdd96d0295f10b2ad746302c2d7bec5d4af3401b318b356d92d437f6bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58836753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601ea6a790f4e830de0248e29607c70ecaf6edd8f15c2f1e93f842f263aaccef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:32:14 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9061cabaf9773189e70b4e71e0890bde5007eaad2b6f09bf883ad9fa1c45f3dd`  
		Last Modified: Wed, 11 May 2022 01:42:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:a7d388b7f97cc67ef137620e27b9390c307f59fcafc812fc15b555508fd219bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53276849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67a35a8f2781240aa5a58044df2b4f5acabe1c27094fb1f5e02cba615163bd6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:39 GMT
ADD file:2aa6033cc58847736587260ccd8559fcc352cb0c91436fe6bc98ff1c0e457cc2 in / 
# Sat, 28 May 2022 00:42:42 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:51 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5729889737c79e488091d7133428cefb547531cac87f70671a7a8def5c83b822`  
		Last Modified: Sat, 28 May 2022 00:49:25 GMT  
		Size: 53.3 MB (53276622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce9feeded7942a32c575e5f9202d060a30597147c28fdbe8bf9e3f58a72738`  
		Last Modified: Sat, 28 May 2022 00:49:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
