## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:56d7da757601389583e8399666fcceedfdd02ce04926411a247e81e80ecb8897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b598f7025d3ae3ebd011318a40961717955b38173406bd655566df6f4a77c119
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71935001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98dbdd3d63fc3e5f2a23c615a575c6d8d33033c07d49cae8d8e03c4dcfe3d51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:03:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:03:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaf1dd00a337044e2c0421947b13d7390883ef55a08ff9ea58d13ce59784328`  
		Last Modified: Thu, 10 Sep 2020 01:16:59 GMT  
		Size: 17.5 MB (17545982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:63d131745d7b939f4e38caf26291c5380ec116443d59fab046772c04b699c123
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69621034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8d1ead31a436872aaaf20bce51680998f9a49610c4fa2a0412d6583ff581f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:15 GMT
ADD file:b5770ada526014c416df31779f0c640c62a5e53e8e018a6201d507999ac34e18 in / 
# Wed, 09 Sep 2020 23:54:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:37:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:37:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:82ebff95f0e21d655344637482b367c7ea0db41b80cbc667bd980d2141287029`  
		Last Modified: Thu, 10 Sep 2020 00:03:15 GMT  
		Size: 52.6 MB (52583713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f40e46cda9c751ff385c796d48a3c39740220c3885866739fe62640f9437afa`  
		Last Modified: Thu, 10 Sep 2020 00:55:04 GMT  
		Size: 17.0 MB (17037321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d4349afe45f16140fec4e1905be9677a58e01759a8ca29508d2e159d7e7da833
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67029154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451a5e116f925ddb06efb756e874aec2536b8abebf2c8fe8a32cd298cea90d91`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:32 GMT
ADD file:6c1ccdfbdb357c0b130cfe85bd05903e56f365e3d93c21c70339151862d2897a in / 
# Thu, 10 Sep 2020 00:08:34 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:44:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:44:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3bf2610be79f89db91594c41fa743370fc433e9e9898fa5d42098ba30efd7f9d`  
		Last Modified: Thu, 10 Sep 2020 00:18:15 GMT  
		Size: 50.3 MB (50305547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9c931dec194117f2ee5eecc8d09f5847406d2a176f0a7256b132a77174e42`  
		Last Modified: Thu, 10 Sep 2020 02:03:12 GMT  
		Size: 16.7 MB (16723607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5168737379fec38db9b5863d1d4fcd284b8cba57ad7d14cfb3d75c2af3a80e92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74465393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d6ca8eff74422d037ad2e5ad78c12f30c25397ae3ceeb8f42980514c016117`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:37 GMT
ADD file:b8a03a5f95e2490a27b297173fd17ea8037e2db6c1619ac9e84d781ff97ecba9 in / 
# Wed, 09 Sep 2020 23:40:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:54:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a11948377c3d4859427c8f59e5f3716e2aba1cb63cc4e9dc8807d8e647dc118`  
		Last Modified: Wed, 09 Sep 2020 23:46:47 GMT  
		Size: 54.6 MB (54609479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bc82823dc8235bc61ea05f4d8421c65972757bede832556e79ce352c099f4`  
		Last Modified: Thu, 10 Sep 2020 02:14:34 GMT  
		Size: 19.9 MB (19855914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
