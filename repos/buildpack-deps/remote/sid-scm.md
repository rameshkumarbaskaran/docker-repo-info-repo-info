## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:7cb195ac6bc6b59650d4ed8d4b7cebe3d29cf904ff2c7de0433cf65ad0666056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:50910903bb3738d2000e11af43cf6b5067e6afd954ee816cd9ce5cabd104b14e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129373016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37e71e8e62c94f3ce5dc0239806c71f7f7150a15dc23207ed0975061c8ebfee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:28 GMT
ADD file:49aaad883f9932e76df5604c9353bdbc51cd2c74b986b57b2dbb4f3aeaa46404 in / 
# Tue, 09 Jun 2020 01:22:28 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:54:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:55:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:516091449b2853b301713d61c7a73bfbe7ae63ace598e76e1d5e9da246f88b37`  
		Last Modified: Tue, 09 Jun 2020 01:27:16 GMT  
		Size: 51.5 MB (51526780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3385de445fd2842a13718698d3fa721fdd723aaede5f9cc079f9bc763e815830`  
		Last Modified: Tue, 09 Jun 2020 02:01:38 GMT  
		Size: 7.9 MB (7920994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd8a6c64c26854ad6d393a2096bb413e86391dc5861cc5a961eb2c55eaa1f63`  
		Last Modified: Tue, 09 Jun 2020 02:01:40 GMT  
		Size: 10.6 MB (10579754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fdc4632caaecd4275038ef75a4d7591fe4f368589453a583a1ee078a8ea6b5`  
		Last Modified: Tue, 09 Jun 2020 02:01:55 GMT  
		Size: 59.3 MB (59345488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1ffc3703d5d8d806589b7d68217ab6f443281d684d6f7afb5cccc89ef09321cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124154430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9770665fc4c619533208e46fed17b03d116f28303fe93360a5a4aab459e3888`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:54:09 GMT
ADD file:333f6925c41655ef86c1c55aa4628d69f324c5f263e27174c329a670a7408728 in / 
# Tue, 09 Jun 2020 00:54:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:39:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:40:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:42:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e514d65a1f93d9b21040cfb52628de87401493f0b2eb92f1a22c9d381f15df3b`  
		Last Modified: Tue, 09 Jun 2020 01:01:40 GMT  
		Size: 49.5 MB (49505780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da95254689f8f0bf61ba2fb5802bcfd31293fb3a56d7c3ee6b7653d100b6e62f`  
		Last Modified: Tue, 09 Jun 2020 02:00:49 GMT  
		Size: 7.5 MB (7500859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e156bd6d1d602264fe07ee2e4da6116f3627a0cdcb05d3f8452ab7e6a15fc5`  
		Last Modified: Tue, 09 Jun 2020 02:00:50 GMT  
		Size: 10.3 MB (10265113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64920f1a1e404f43b9ad025af513da62eb1e49466c92adafed377f2c5543974`  
		Last Modified: Tue, 09 Jun 2020 02:01:18 GMT  
		Size: 56.9 MB (56882678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f10a49002e4952b5a00c15a1c0084653d1afb58c98f08b10a61bab15ed14f77
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118915326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d38d3b89ac4a92da153a2f11e25019c509af577fbe9becc71a501225a2fda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:04:25 GMT
ADD file:f137ab200a6655933430876a9a0f3c675ed39dbf4a73be4750579b0c66812888 in / 
# Tue, 09 Jun 2020 01:04:32 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:59:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:369ddd165e2326d11cacb52bac2afd8d2277bc9506399fb693a5a5eb336716ee`  
		Last Modified: Tue, 09 Jun 2020 01:12:30 GMT  
		Size: 47.3 MB (47326325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ada3ce7a1b468f31af8a1aa9f083d4521fbeedd0d46757dc5d1f97c49ebf17`  
		Last Modified: Tue, 09 Jun 2020 02:13:48 GMT  
		Size: 7.2 MB (7243269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab399397acddc3f7ce3a847871519a272a15f91ee26bd786a485bf8a41dc870`  
		Last Modified: Tue, 09 Jun 2020 02:13:50 GMT  
		Size: 9.9 MB (9916653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfd7032d9f8bf51476a074156f4ebd7aa42e52d8e07b6e899f787d2eb56a14b`  
		Last Modified: Tue, 09 Jun 2020 02:14:15 GMT  
		Size: 54.4 MB (54429079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9249dc5d006c74d2bba8c4a4d81ffe8f906e177455e8ff7cf2ef369f2e2752db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128343865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869f334301866238336d3692b678f8d3fbdad3c99347025c3794d17da7ce4e38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:53:03 GMT
ADD file:56e3fbb5c1d0a4c301b36e4f85f596b26f32562da8ed0a704496f1e3ca5c676a in / 
# Tue, 09 Jun 2020 01:53:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:35:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:35:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:36:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f925f2558464755f2d5e30c33f6f9072851b0da5fb44204c52fcecdfb3bfbb44`  
		Last Modified: Tue, 09 Jun 2020 01:59:06 GMT  
		Size: 50.5 MB (50491571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b751eeb6110560d41a2af99cdea392104b87433a0ba6fd41a17872f77369f134`  
		Last Modified: Tue, 09 Jun 2020 02:48:52 GMT  
		Size: 7.8 MB (7795590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284f1451ccb4e8af4e45ad26e876fb36dc52c07dd21d5c4b226f8ac6a9407fba`  
		Last Modified: Tue, 09 Jun 2020 02:48:51 GMT  
		Size: 10.6 MB (10588456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4f07de830aebf1a95a75c20d01a9d7b137067dcc03270e4b2817c78bdb0bb`  
		Last Modified: Tue, 09 Jun 2020 02:49:16 GMT  
		Size: 59.5 MB (59468248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:23a0aa37bd750c27cad3e88a699cb65032046d92f078e2b161641a91f252027a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133186127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50240b6fff76223187c0a80cae8450ddcaedc1216c446af6d572d928b257d813`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:41:24 GMT
ADD file:e46d18aaa3cf0eb6320c1b26b025ee8fbec78b2c4e4b3f5d4343393f1cbc769b in / 
# Tue, 09 Jun 2020 01:41:24 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:23:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:24:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:24:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c73d5896f1a36fe56b17fa2ffd2771c0b97b78e1b086e696cfa14b05618bbeee`  
		Last Modified: Tue, 09 Jun 2020 01:47:08 GMT  
		Size: 52.6 MB (52644936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf148f44d6df7cce1b2964667971df2c24df9d24505794d9324b303eff4da0b`  
		Last Modified: Tue, 09 Jun 2020 02:35:07 GMT  
		Size: 8.1 MB (8099472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa8c598f01778284c7219a5d6e3853bc2247c68a8e1ce0851af567867177c31`  
		Last Modified: Tue, 09 Jun 2020 02:35:07 GMT  
		Size: 11.0 MB (10960005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c50a355d1547fd485f5847386487c1b5c9e1b423bb328cfa13d40d4ccf5709d`  
		Last Modified: Tue, 09 Jun 2020 02:35:36 GMT  
		Size: 61.5 MB (61481714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a34a1ab183c41c55c6d1a85f6bdf604ed44f49f13e83893948d6afe406399048
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126567225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cbaceb0ab4fbbebd520594e008dd85c6a8c7621dec0420ca9811c1792f90dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:11:18 GMT
ADD file:2c0e5d72dc26223a4df660e91acd4c8c70d1b0ee1139c92fb9cb3f041d81bdc2 in / 
# Tue, 09 Jun 2020 01:11:19 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:56:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:56:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:57:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:78e0a34f3ecd34b89d20cdb0b915427acd1691184f4f7649f816759737ddb842`  
		Last Modified: Tue, 09 Jun 2020 01:20:19 GMT  
		Size: 50.3 MB (50264875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff174bb9582ec89056fe600d1820b6c6e7445d74e52537dfea39a4dd2b4324e`  
		Last Modified: Tue, 09 Jun 2020 02:14:03 GMT  
		Size: 7.4 MB (7447530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44807d6533dba987e8712d4b69466283e5bbe760298ac86ccbe1ed4ea542e2`  
		Last Modified: Tue, 09 Jun 2020 02:14:05 GMT  
		Size: 10.6 MB (10598855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46849a421d1ddb3755126f8b58c93389f656c6533dd46480416ce5fe6af98d6`  
		Last Modified: Tue, 09 Jun 2020 02:15:04 GMT  
		Size: 58.3 MB (58255965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d639746073589cca1f4559b903b7b815b28c51ddeeb59ad263a011f45a060002
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140093207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69785aea7178aa8c1d79a63f8c01c7d9648b49e63aa085ffb75848f8fec1f92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:47 GMT
ADD file:04723d2d8de7d77c2c146c6af521e4a3124ca84c794e6ab9811528805e9f8a16 in / 
# Tue, 09 Jun 2020 01:23:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:13:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 03:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57bdb75510f480914b31ba736d52f2bab13d126b2808f87359f0678e25b38717`  
		Last Modified: Tue, 09 Jun 2020 01:33:30 GMT  
		Size: 55.3 MB (55274450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c7f2f7dc07ba0a3435ca28dca3bc46cfbf238c2fd76e208d4b394f7a1de537`  
		Last Modified: Tue, 09 Jun 2020 03:46:48 GMT  
		Size: 8.3 MB (8346012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a7d75882c1ba6c6a4c7b499aa5bd492b3bfebc6670ca2c2c3dac6675be974`  
		Last Modified: Tue, 09 Jun 2020 03:46:47 GMT  
		Size: 11.3 MB (11326929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a723bc74187577bcfba79dff09ce9808d81478c829672c29f518b83f20218c`  
		Last Modified: Tue, 09 Jun 2020 03:47:41 GMT  
		Size: 65.1 MB (65145816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4dca5503bae51f1a2da2084db2d1ee99eba562713652316db5422e04b72bb838
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126720368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9efc6ff8d0fef004eac86280c0945d288e069d0e781a7b10c242ca3f55e2b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:43:14 GMT
ADD file:f1ebbcfe99a36749cfce4bf2c38aff7e5a06ff0eee49c1c44970cb518d59c6c1 in / 
# Tue, 09 Jun 2020 01:43:17 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:11:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:11:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68d68a3a62e23bc275e3488ccf04bd3d9cf392e7f00f7ac29a6f1d74be8ec63f`  
		Last Modified: Tue, 09 Jun 2020 01:47:06 GMT  
		Size: 50.2 MB (50155657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69552bf02d312240efc0fa7fe7d03054f5a709076df8a08878cd0782b3cac8b`  
		Last Modified: Tue, 09 Jun 2020 02:18:53 GMT  
		Size: 7.6 MB (7589963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77d73b4136a153380a7e5348a698053b0ee98f961fe50d20e65ca30de8da8d`  
		Last Modified: Tue, 09 Jun 2020 02:18:53 GMT  
		Size: 10.5 MB (10456030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895be31368f26dc7d04d4c9a689adae6dddc460d56bca91594be43fed86789a`  
		Last Modified: Tue, 09 Jun 2020 02:19:08 GMT  
		Size: 58.5 MB (58518718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
