<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:35`](#fedora35)
-	[`fedora:36`](#fedora36)
-	[`fedora:37`](#fedora37)
-	[`fedora:38`](#fedora38)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:35`

```console
$ docker pull fedora@sha256:6a4d2e5877801432b386673d4e6f99ba80697c82e792e64bc72d8c7bde5128e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:35` - linux; amd64

```console
$ docker pull fedora@sha256:8e5852e0a72101197de788437844ae9e1b382b719ba7ac7cf482804e0ffa04f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55740531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d0cdfd5d956c392500708fbb1c82aa81a5e51c75c68448bd411ece20cde2f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 23:02:34 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Thu, 03 Nov 2022 20:40:27 GMT
ADD file:f696eb87c7de0bd8a2b1679c7d4cb0e3a0b284278592e1e6082b16368b1b02fe in / 
# Thu, 03 Nov 2022 20:40:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6153fc78ad283cb10dc19fe1a49cc6c088872832764bb163196041ea3cde666e`  
		Last Modified: Thu, 03 Nov 2022 20:41:31 GMT  
		Size: 55.7 MB (55740531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:35` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:7b40faed46696792a3e00765a5c36a727a615b77aff36d236e4502f9c1761305
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54726098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559c7022f8c4abadb8c357fbd78e855d8306e08396bd0d40527b1eb10a353dab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:13 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Tue, 15 Nov 2022 23:24:20 GMT
ADD file:3fea7fc7b342e30f44849f2700d3377c80f69906780db98907fb599b42b45351 in / 
# Tue, 15 Nov 2022 23:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fcd22a724e2b82fe984fb29805cd31045807bb47dec5d323597368761c35f5d8`  
		Last Modified: Tue, 15 Nov 2022 23:25:09 GMT  
		Size: 54.7 MB (54726098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:35` - linux; ppc64le

```console
$ docker pull fedora@sha256:60b722cb640221e50943c5a8801099ba61004ffe36f1dbc5a3c52225acfb6327
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60682412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cae0f2e6393f816b38b6c0acc95a5b58bd27cda534bdc485870b9ce72b705c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:07 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Thu, 03 Nov 2022 21:17:57 GMT
ADD file:9b16c5218009e478c7b88b71868237f62ab6e258533618f342b85dd58206347b in / 
# Thu, 03 Nov 2022 21:17:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab5754c22ec4f84a6ecabe786e2bd2a40b91174d8b871fd5ab885ff6132f00e0`  
		Last Modified: Thu, 03 Nov 2022 21:19:57 GMT  
		Size: 60.7 MB (60682412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:35` - linux; s390x

```console
$ docker pull fedora@sha256:5fe28dd9802b8ca73da022076a971c34bd4b47f9c5c3a6a4af17f89a03dc5503
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53726138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceb5312bc855adff593a8d652666f6802800b53bc9295f71a2383f3e065da2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 22:42:23 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Wed, 16 Nov 2022 02:10:01 GMT
ADD file:dc52d9ac55b509b188f0a0d4b35b3c206dc023d1988e062925e07759eb1be36f in / 
# Wed, 16 Nov 2022 02:10:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76a7ae73c8a1e0ab4275e6372995cd901e1b9bead458ede839d28827c3ed39e9`  
		Last Modified: Wed, 16 Nov 2022 02:12:23 GMT  
		Size: 53.7 MB (53726138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:36`

```console
$ docker pull fedora@sha256:a791d718fc81ee3c300cf95b005b13bb93c3d96c7955fa44647a5633c54d7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:36` - linux; amd64

```console
$ docker pull fedora@sha256:455fec9590de794fbc21f61dbc7e90bf9918b58492d2a03fa269c09db47b43f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59995747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7654d129a8a25626dce55adfa5d8a419b794952229ed9542968ef7faca2ee975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 20 Mar 2022 10:46:00 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 20:40:40 GMT
ADD file:8d61743db71ec38169aae6644f4ef369766e0bece381549d7530d11df9a9a214 in / 
# Thu, 03 Nov 2022 20:40:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e437052d4f94147f80c5b03d10b6d7e034a32b1db5a9f340b2c8090cec1376f8`  
		Last Modified: Thu, 03 Nov 2022 20:41:48 GMT  
		Size: 60.0 MB (59995747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:36` - linux; arm variant v7

```console
$ docker pull fedora@sha256:ce3d46c564d9145f73d1618a605e9d959ec704d409b2afb54f3517a27c818cc6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54490837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6e76519a089477b47efb6d84e8dcbc6639cc6a12e03d575b069278e4cffa88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 20:46:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:46:50 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 20:46:56 GMT
ADD file:2a100119d250f9a75cfee4425142172c6ec02864e33737f0dd9e8330ccecce4a in / 
# Thu, 03 Nov 2022 20:46:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af068febaa0f76501a770f13db16f57d1900b8d9c746a4ec074e4c234de151b5`  
		Last Modified: Thu, 03 Nov 2022 20:47:22 GMT  
		Size: 54.5 MB (54490837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:36` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:9d69bc093f7e25dd2bb5be722c65184b1e81b09c9723dc7774e23e73f09e47bb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58095294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bbe89aa2e8ebe895a35b606dbb804613567a07282a240b2f0e01ab7d6e10f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:22 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Tue, 15 Nov 2022 23:24:31 GMT
ADD file:ae75cec0600ced074820dfb39828c1e391ba071b5be13331d6365c17cacda8a4 in / 
# Tue, 15 Nov 2022 23:24:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b45cb1c301f75fdf0ca9c423717529694f0803125c407c0b3e81d79f68719edd`  
		Last Modified: Tue, 15 Nov 2022 23:25:22 GMT  
		Size: 58.1 MB (58095294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:36` - linux; ppc64le

```console
$ docker pull fedora@sha256:72ed15e0fd3d47ae2f15282121a16a70e1e160450dd7a5c18f929904e86dff16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65410552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e5939540b7d8a7c6688a99727185fdba334c9badb2ebd87277fdba08e936e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:27 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 21:18:22 GMT
ADD file:1d9d84b7845e61a4beda77c6785383e27562f7e2fb2bcfb54ccd4138b2730c3c in / 
# Thu, 03 Nov 2022 21:18:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ad8408f5b2d2dd65fa3ca093ea3b2dbbb1e17e0320fb0d56ae86c11352f276a`  
		Last Modified: Thu, 03 Nov 2022 21:20:23 GMT  
		Size: 65.4 MB (65410552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:36` - linux; s390x

```console
$ docker pull fedora@sha256:a7526b4aba5f4fdb40c30e294736c805ed8ed4fb9cd145e0c8ac952230af1ed3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56999067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0685b250d52688385ccad5bebc4257a4fa7f1178bb53b5dc5d55d08cb72051`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:33 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Wed, 16 Nov 2022 02:10:26 GMT
ADD file:60741c0f2e62bc9eb43e65126a9c6d5559a23efb676b74e3bd3eef7f4cdd83ff in / 
# Wed, 16 Nov 2022 02:10:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a82130d5e6208da653601a574c2add3000abb37e4be4442f04b4711225152999`  
		Last Modified: Wed, 16 Nov 2022 02:12:35 GMT  
		Size: 57.0 MB (56999067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:37`

```console
$ docker pull fedora@sha256:762f2ef5f8282c6188c3cec0be7a97d143aa79a40d4514dbb366cd6b2bd73f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:37` - linux; amd64

```console
$ docker pull fedora@sha256:6184fcbfc8f27fda21d0f7a69c74b0f7bcd1a61ac9b566b8d6a3a3adefad1657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65990425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b88d41f1c8cc270ffcb792f1e914928c148f8f0620ca5de6e384767e57369e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 20 Mar 2022 10:46:14 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Thu, 03 Nov 2022 20:40:54 GMT
ADD file:0226ce47da6a83519e0692ec1a9c5b587dc79a25d69ebeeaedc3780074f29d21 in / 
# Thu, 03 Nov 2022 20:40:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0798f1d8aae23f95c245d28fd50b7c68bee321534c9809612e323eb988c2b3a4`  
		Last Modified: Thu, 03 Nov 2022 20:42:08 GMT  
		Size: 66.0 MB (65990425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:0505722995b79a8b2c213ddc0a6455928c5f7dbf5853bc7fca9e32912eee204a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023f406571ec80fbe203c9b6bf501eb5351d9d488f1787aafaea9b27601c0884`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:31 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 15 Nov 2022 23:24:39 GMT
ADD file:a488961f8a8b61bd750e575946cbb7b5c70474c7f836c05967a08a394e67c289 in / 
# Tue, 15 Nov 2022 23:24:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:561df0e9ba64f8ec496b4725756bd764608666507e5de547ba686d2a99ad5021`  
		Last Modified: Tue, 15 Nov 2022 23:25:35 GMT  
		Size: 64.2 MB (64208303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; ppc64le

```console
$ docker pull fedora@sha256:f54ba1eacd025e9fe50e8ccb92dd9fa106f3468f283655894bc68c434e97966d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71682863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8d3c9f069634c4cee7af46a23ac3a873bb598cb7c4c2f17832068612c5f1ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:51 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Thu, 03 Nov 2022 21:18:47 GMT
ADD file:bba6b2c837ef0a16d2b77ae80936001432060d29808972351ac2a64147c6489c in / 
# Thu, 03 Nov 2022 21:18:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8e1b4c7dc67dab15b509d7f6703cfd23a62d9288837a87c02bcbfd115011ece7`  
		Last Modified: Thu, 03 Nov 2022 21:20:55 GMT  
		Size: 71.7 MB (71682863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; s390x

```console
$ docker pull fedora@sha256:a7fcd22632ccd8e88e19940725fc3a84ac5e948b37498e41ae879c8a60bc6136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63155468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63af148a00e062b8076537fb1fc8f46a1281c5cce4c287f6afcf9a77f98344fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:50 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Wed, 16 Nov 2022 02:10:53 GMT
ADD file:7328e1dcc3a055cba614512b0dee3890f502896decf9eb0ea8078664bfb790e2 in / 
# Wed, 16 Nov 2022 02:11:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8d0cc138a373e92ff38a361658afb9b131524ee38d8c17d758ec136e913ad5d`  
		Last Modified: Wed, 16 Nov 2022 02:12:48 GMT  
		Size: 63.2 MB (63155468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:38`

```console
$ docker pull fedora@sha256:b94a6db40f6192210ea19e4db9aaf24b5d3e5cf8ab38023b9e479afb6dae4906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:38` - linux; amd64

```console
$ docker pull fedora@sha256:c7dfa518d9db440fb02362c0f9b014c0e1b8e04bc0f6bf540d1d5ac2ecb43453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902325de1ec96bbbeecd610ef5dcfba06da72e6831eb0ac1049e376d7778a58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 20:41:08 GMT
ADD file:aea454c4f9f7bccbd03cf61c6477deac629e6b63f8ef39d87667ee4efaf12136 in / 
# Thu, 03 Nov 2022 20:41:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7658a6d4e9efd0ec04b7aca3c754f4441c79d4dedab19a67c5f5293bb0b5e151`  
		Last Modified: Thu, 03 Nov 2022 20:42:25 GMT  
		Size: 65.6 MB (65568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:6e1160094641e19b3ae1aa45382edf003115ed80e7a5eb70920d25f222cef6a7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64031417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4270e03b1e788ad9f22db2069ca5f46b3b0d202151f26f730d632fbfaabb322a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 15 Nov 2022 23:24:49 GMT
ADD file:f3f02cd039386200c4016153c08090962456cb51379aba9fba1a1523210cab8b in / 
# Tue, 15 Nov 2022 23:24:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:803d75c05eb7ae8a4fdb882e5c8794f4ccd3fd48d9f20dff418bc5f35002e881`  
		Last Modified: Tue, 15 Nov 2022 23:25:51 GMT  
		Size: 64.0 MB (64031417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; ppc64le

```console
$ docker pull fedora@sha256:bbc10a3fd25705b990ffa3c3fefa49911129c29763a9a66c301bf30a927e3afa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71231033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b6a61a694cd3ae5798c3ca7b97f8278e0dc054bbd5b8fd1e33d33e3cdf767b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 21:19:13 GMT
ADD file:c5bf5b641727fb8e7c31aa41672e0ddb05df5c6eaf89a0f843077ca40a47fc7c in / 
# Thu, 03 Nov 2022 21:19:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd28bd1e5a238b01fff9e8ef41017687d39ab4bc32b334d1e20bd91365c70797`  
		Last Modified: Thu, 03 Nov 2022 21:21:22 GMT  
		Size: 71.2 MB (71231033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; s390x

```console
$ docker pull fedora@sha256:6588fbf39a732e1565dd86a964aa887b6ec01d30dc663d2e2559cf7f819275b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63181632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc5bb1579778fdd05c25d2150e102989bdd6dc56474d36ee47708eaf3219b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 16 Nov 2022 02:11:20 GMT
ADD file:47f6a01ddbce4bf76d1552556ea134308b7e18a706904729ee640b92a5fb081c in / 
# Wed, 16 Nov 2022 02:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb5c3098cd40cba591630ca5088f79ef283785dca831281a621120e480e49f71`  
		Last Modified: Wed, 16 Nov 2022 02:13:03 GMT  
		Size: 63.2 MB (63181632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:latest`

```console
$ docker pull fedora@sha256:3973cf968f9c1b25d68d495815b5a47e350f3986524aee86cfa228f828a58564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:455fec9590de794fbc21f61dbc7e90bf9918b58492d2a03fa269c09db47b43f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59995747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7654d129a8a25626dce55adfa5d8a419b794952229ed9542968ef7faca2ee975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 20 Mar 2022 10:46:00 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 20:40:40 GMT
ADD file:8d61743db71ec38169aae6644f4ef369766e0bece381549d7530d11df9a9a214 in / 
# Thu, 03 Nov 2022 20:40:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e437052d4f94147f80c5b03d10b6d7e034a32b1db5a9f340b2c8090cec1376f8`  
		Last Modified: Thu, 03 Nov 2022 20:41:48 GMT  
		Size: 60.0 MB (59995747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:0505722995b79a8b2c213ddc0a6455928c5f7dbf5853bc7fca9e32912eee204a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023f406571ec80fbe203c9b6bf501eb5351d9d488f1787aafaea9b27601c0884`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:31 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 15 Nov 2022 23:24:39 GMT
ADD file:a488961f8a8b61bd750e575946cbb7b5c70474c7f836c05967a08a394e67c289 in / 
# Tue, 15 Nov 2022 23:24:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:561df0e9ba64f8ec496b4725756bd764608666507e5de547ba686d2a99ad5021`  
		Last Modified: Tue, 15 Nov 2022 23:25:35 GMT  
		Size: 64.2 MB (64208303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:72ed15e0fd3d47ae2f15282121a16a70e1e160450dd7a5c18f929904e86dff16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65410552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e5939540b7d8a7c6688a99727185fdba334c9badb2ebd87277fdba08e936e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:27 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 21:18:22 GMT
ADD file:1d9d84b7845e61a4beda77c6785383e27562f7e2fb2bcfb54ccd4138b2730c3c in / 
# Thu, 03 Nov 2022 21:18:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ad8408f5b2d2dd65fa3ca093ea3b2dbbb1e17e0320fb0d56ae86c11352f276a`  
		Last Modified: Thu, 03 Nov 2022 21:20:23 GMT  
		Size: 65.4 MB (65410552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:a7fcd22632ccd8e88e19940725fc3a84ac5e948b37498e41ae879c8a60bc6136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63155468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63af148a00e062b8076537fb1fc8f46a1281c5cce4c287f6afcf9a77f98344fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:50 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Wed, 16 Nov 2022 02:10:53 GMT
ADD file:7328e1dcc3a055cba614512b0dee3890f502896decf9eb0ea8078664bfb790e2 in / 
# Wed, 16 Nov 2022 02:11:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8d0cc138a373e92ff38a361658afb9b131524ee38d8c17d758ec136e913ad5d`  
		Last Modified: Wed, 16 Nov 2022 02:12:48 GMT  
		Size: 63.2 MB (63155468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:rawhide`

```console
$ docker pull fedora@sha256:b94a6db40f6192210ea19e4db9aaf24b5d3e5cf8ab38023b9e479afb6dae4906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:c7dfa518d9db440fb02362c0f9b014c0e1b8e04bc0f6bf540d1d5ac2ecb43453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902325de1ec96bbbeecd610ef5dcfba06da72e6831eb0ac1049e376d7778a58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 20:41:08 GMT
ADD file:aea454c4f9f7bccbd03cf61c6477deac629e6b63f8ef39d87667ee4efaf12136 in / 
# Thu, 03 Nov 2022 20:41:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7658a6d4e9efd0ec04b7aca3c754f4441c79d4dedab19a67c5f5293bb0b5e151`  
		Last Modified: Thu, 03 Nov 2022 20:42:25 GMT  
		Size: 65.6 MB (65568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:6e1160094641e19b3ae1aa45382edf003115ed80e7a5eb70920d25f222cef6a7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64031417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4270e03b1e788ad9f22db2069ca5f46b3b0d202151f26f730d632fbfaabb322a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 15 Nov 2022 23:24:49 GMT
ADD file:f3f02cd039386200c4016153c08090962456cb51379aba9fba1a1523210cab8b in / 
# Tue, 15 Nov 2022 23:24:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:803d75c05eb7ae8a4fdb882e5c8794f4ccd3fd48d9f20dff418bc5f35002e881`  
		Last Modified: Tue, 15 Nov 2022 23:25:51 GMT  
		Size: 64.0 MB (64031417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:bbc10a3fd25705b990ffa3c3fefa49911129c29763a9a66c301bf30a927e3afa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71231033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b6a61a694cd3ae5798c3ca7b97f8278e0dc054bbd5b8fd1e33d33e3cdf767b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 21:19:13 GMT
ADD file:c5bf5b641727fb8e7c31aa41672e0ddb05df5c6eaf89a0f843077ca40a47fc7c in / 
# Thu, 03 Nov 2022 21:19:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd28bd1e5a238b01fff9e8ef41017687d39ab4bc32b334d1e20bd91365c70797`  
		Last Modified: Thu, 03 Nov 2022 21:21:22 GMT  
		Size: 71.2 MB (71231033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:6588fbf39a732e1565dd86a964aa887b6ec01d30dc663d2e2559cf7f819275b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63181632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc5bb1579778fdd05c25d2150e102989bdd6dc56474d36ee47708eaf3219b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 16 Nov 2022 02:11:20 GMT
ADD file:47f6a01ddbce4bf76d1552556ea134308b7e18a706904729ee640b92a5fb081c in / 
# Wed, 16 Nov 2022 02:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cb5c3098cd40cba591630ca5088f79ef283785dca831281a621120e480e49f71`  
		Last Modified: Wed, 16 Nov 2022 02:13:03 GMT  
		Size: 63.2 MB (63181632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
