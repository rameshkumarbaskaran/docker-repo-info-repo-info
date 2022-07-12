## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:be9b087e7b6dd383cbbe55025f5b260eaff0bdf5a2b18bd37dd35878b270934f
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
$ docker pull debian@sha256:8971deabea664a0b341f02fddbb5205a63e1470af5c0383a378a351e222d0930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50441011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c513fb1a5dd666aaf5b745dbae58ff914487ca051b2cbae2f9ee11aa4cd210e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:14 GMT
ADD file:cc42a7d35200c41a033897dcc1bc1b1ddc70951895c7b7437852c8207ecdc432 in / 
# Thu, 23 Jun 2022 00:21:14 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:21:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a968030a9a193719b095406e53dc080102416bd788bf2ada491ec6974341e34e`  
		Last Modified: Thu, 23 Jun 2022 00:27:52 GMT  
		Size: 50.4 MB (50440787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1f7cd3cefbcfd2a79050bc6b56ab31120fc08a80a5b58f43e25fa0ddd966c5`  
		Last Modified: Thu, 23 Jun 2022 00:28:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d8610af371632729c53c49d8a4a3df19e237924eb59d22b93b5c63f40725cad9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48160770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fece7754ded2689e21cc737067fcea66895fe826fafd16dc614c61faa1fc404`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:52:08 GMT
ADD file:c548c4d5c56882a23816d6daf3fecf810930a517c6c595d0e3f74a96c9dee434 in / 
# Tue, 12 Jul 2022 00:52:09 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:52:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:219f68772cc028ce2582e6e602379a0b22760bf798aea67e7d34e2b900c3be0c`  
		Last Modified: Tue, 12 Jul 2022 01:05:19 GMT  
		Size: 48.2 MB (48160543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf08d463d987066c84111d9ecdf9588ae789352c665f656a2ad916d340dfd03`  
		Last Modified: Tue, 12 Jul 2022 01:05:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:980c785334e5f8d64f66588cd92b8c9798add485aa968267337ccdca52063540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e47c37d98ae442c15f65452d511874186be7bd62251ef9abae47bc2e4e1c3a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:02:16 GMT
ADD file:28bcd1219a77728f9d7a74b36844de473d1b6400a2a87deb6fb0d7993f2ff790 in / 
# Thu, 23 Jun 2022 01:02:17 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:02:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c89ce61fc8b89745cd320b95306ded5dde5b9b933377da870a6ddfa045ed645a`  
		Last Modified: Thu, 23 Jun 2022 01:18:38 GMT  
		Size: 45.9 MB (45915756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3d2d9eab63b724b9675d8413f26d289917ecc7ffad0748a41f3d1a7fab63f8`  
		Last Modified: Thu, 23 Jun 2022 01:18:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:58fc8c3fed5baf42b9cd0eede93c7781f4accce5ab47b2342bdb62e374fd235f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942373d930548dc66c6a52a511c2ddf1018c3aa13c0274a730ae5e0812204423`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:14 GMT
ADD file:d44e3485a1d35f776fb5bc1a9d0fe0aa82f05252f6797fd603393f82ebaa7072 in / 
# Tue, 12 Jul 2022 00:41:15 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04a0dbfdc60816cff83e8a5a8c741bb057cab6ad6f67ff70824bcf973dbb84bb`  
		Last Modified: Tue, 12 Jul 2022 00:47:37 GMT  
		Size: 49.2 MB (49228925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a71085271a6418455625df4ad697d0c590c6217a675c02f666c4416c2ddf4e`  
		Last Modified: Tue, 12 Jul 2022 00:47:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:bdac90928145cf2a991e76a778c70d0a62e5de8ed6e6c69b2ae18f1c132612fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d08d7fab9a215f14a553dc0d7094a112350db546d508c89bf280a91a3d3a3aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:07 GMT
ADD file:9bf85d9565a376f855995ef65d6714d83ddf3ab0bbb1987b484e8dc3518e078b in / 
# Tue, 12 Jul 2022 00:40:08 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:40:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5120b98fe4ffa160b64a47d9c28e92f5f98cfcb24ace97cda5b6a5406fd4c0be`  
		Last Modified: Tue, 12 Jul 2022 00:46:37 GMT  
		Size: 51.2 MB (51204011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce7a957163631c56f3e979193cbbf8d25f6218b5c916e0d7acc70b78caa995c`  
		Last Modified: Tue, 12 Jul 2022 00:46:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:32628dded01b0259cdd9b7f374adc7c1b050493d8c81533310617f5f151ec09a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49073390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a196a3f54465c6f8c7f21e6babef0c7857abdf3b0f02a6b0610c8b4c8f572459`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:12:00 GMT
ADD file:c3d178ae439b5eec9d9da797f6caa9d15b3faebf34eba6dbd3ce190687560359 in / 
# Thu, 23 Jun 2022 01:12:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec3cde1adfbde3bc6f7df479b50e746a548a93317390faad2a0c13bf62044f6c`  
		Last Modified: Thu, 23 Jun 2022 01:22:28 GMT  
		Size: 49.1 MB (49073163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f78ac6af604716ef7795b763e492aa056cf3ff5cdea13f7d222329291706ff`  
		Last Modified: Thu, 23 Jun 2022 01:22:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4873c9031a7fd9cdb327300f44a8f94f8dea7629231ed8f29e264db0ac77c322
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54177319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d848d831806a1a727520254b2e37d1d00b09a027c881217fff4376c27a63ee13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:51 GMT
ADD file:2f29e572d6d86d405fe9c5b5b6387519e0b81fee8d0d526265a210ca69912ee4 in / 
# Thu, 23 Jun 2022 02:03:56 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:04:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f4ac77bd915694d48ea8176a9c993e70268a24e1d2c0f136b17a242531279377`  
		Last Modified: Thu, 23 Jun 2022 02:19:07 GMT  
		Size: 54.2 MB (54177092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67fad859ea93c945ade096fd68c006ca6cdc00c8f688c9738d74bebd539e340`  
		Last Modified: Thu, 23 Jun 2022 02:19:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:f3f3461125cad05d64b872bdd148764bd2a5249286fc79142e41f350bdb5cb1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776cc1762f3d5bb46967fcaced6a5fb03a49669996817c1b58df18f8a111bba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:45:09 GMT
ADD file:1ef8c265d400d0a107411523dcb599b4632879c5ae488cf7df291f14c6ca0709 in / 
# Tue, 12 Jul 2022 00:45:16 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:45:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbd1e6327db48cec9d4b9bbea1ecfdd4a95a4e1521fccf75f6d61a084bba1573`  
		Last Modified: Tue, 12 Jul 2022 00:54:39 GMT  
		Size: 49.0 MB (49006980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2ec8bf591e3bf7b2d8a6762f26ebf8da3bb1670df41c906cdfdf283c56ba5`  
		Last Modified: Tue, 12 Jul 2022 00:54:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
