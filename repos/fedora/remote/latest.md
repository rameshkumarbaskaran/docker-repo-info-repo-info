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
