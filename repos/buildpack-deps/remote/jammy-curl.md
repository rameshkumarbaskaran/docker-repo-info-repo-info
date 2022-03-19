## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:a54f4af31a529c21aa75c11c707d2be1792783011f317e38ab7f3fb4a0aa9ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1e05839f1a1496695c5056666281f4324ecebe5221ef4235d1c35665907c24bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37862839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62980bdfe9568899ff86700e0c5c94890e6165de7e24bd36d4480cb24c1bb795`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:31:09 GMT
ADD file:ce9bee138da151fa0b9e441f7ef06865e0171006e686f0dc5e1ca6a06e0a3d0c in / 
# Fri, 18 Mar 2022 05:31:09 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:56:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:11581404396c9d08d16b97c64bb2fd043ef3216bd3e3ff3d1c6e03398dc8e336`  
		Last Modified: Wed, 16 Mar 2022 11:30:57 GMT  
		Size: 30.5 MB (30485551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1305491a76442ac63301690c078bd5fc0af516ba25fde9528a35db9188c4e2`  
		Last Modified: Fri, 18 Mar 2022 07:12:40 GMT  
		Size: 3.8 MB (3817797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a1be61110601cb14ca88a066963bb29f75059eac2b2f9fb7a60196a2c46667`  
		Last Modified: Fri, 18 Mar 2022 07:12:40 GMT  
		Size: 3.6 MB (3559491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2d021a2cd2a72f4f943ed1cff7ae817d35c381668b222a5a5d5e9457e269f738
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34349833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dedd8041f79c70902694767d5dc45df4a4cc55faacc2cb34ab8ed54448a32b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 07:33:30 GMT
ADD file:19a0584ac22c220c1260894e828ead25579919ba2a0448fb8bcf90ba5dc4ca07 in / 
# Fri, 18 Mar 2022 07:33:31 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:18:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:559c58962576ae20efaf4338d13982a09d934fa524ef90330d051b6ebcb20608`  
		Last Modified: Fri, 18 Mar 2022 07:37:29 GMT  
		Size: 27.1 MB (27069048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2098a0e581836f2c68e2c4dcdf61d703be4f4ad972816519300cfeb2ff2bb8c`  
		Last Modified: Sat, 19 Mar 2022 03:49:33 GMT  
		Size: 3.6 MB (3568653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4415fb5c74607390e5a07fdef46a85e56c4f53013f42bbe83c307ac1ef516`  
		Last Modified: Sat, 19 Mar 2022 03:49:32 GMT  
		Size: 3.7 MB (3712132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e5c3efa10b67d782328849e5f629621d27a31f36e7f2549dcafe969b66f5cc36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35536421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b25908b032c2e2074fec2d107ca79587f4eb0f945bdf213b088f7a453c8cc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:41:10 GMT
ADD file:c81be95ae491788086dc606dd86ac47b679f2ce48c96016d4ba321e995541bca in / 
# Fri, 18 Mar 2022 00:41:11 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:19:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:19:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8037d5c930bd3f2cc0b5ef6849e32124c3c5efaf4389d0974934bba554464390`  
		Last Modified: Fri, 18 Mar 2022 00:43:17 GMT  
		Size: 28.4 MB (28425528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c4c183bea4a76f9fa90d8efd82e02a12f5ecf6f00980a88a5315cdb0d54229`  
		Last Modified: Sat, 19 Mar 2022 15:26:51 GMT  
		Size: 3.8 MB (3791931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0bdf9cb2789894c77a5708b46d74b9f6969ba0ac0d6fdc8db894179e474345`  
		Last Modified: Sat, 19 Mar 2022 15:26:51 GMT  
		Size: 3.3 MB (3318962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e87971830e099c6f824534c8738c9b9f2cbc7b06d83e82b05058c0558b83a1a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35178972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c64b55a573abe229e984b4deed2e6b6df58834b5d766a9f515c8b940a11711`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:43:01 GMT
ADD file:5596c6fcfdc9d3c4b63db527cacb4cac548690f6631b60dee4972329037237c1 in / 
# Fri, 18 Mar 2022 00:43:02 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:12:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:779c5da60b9290c00c305c706d5d477b0647cc028035cc1723db7e437a962fd8`  
		Last Modified: Fri, 18 Mar 2022 01:01:57 GMT  
		Size: 27.8 MB (27792674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d84b474ce4102d31d6fd8cea63267bfece598ec610fe1f5612b795b0960831`  
		Last Modified: Fri, 18 Mar 2022 03:49:04 GMT  
		Size: 3.6 MB (3611244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4323e0585e69caede2372dd7a23853990eae0fe4e7d87d98456fda8e0f48e7ea`  
		Last Modified: Fri, 18 Mar 2022 03:49:03 GMT  
		Size: 3.8 MB (3775054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f07adb488ecd026833c0224e05bbf0c4339da9e32706a87788a5c8c44ce899a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36012949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d063331df1af763ee326f9ab90d84b0e99be8e4b5c776fdb76ea14a95afdc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:36 GMT
ADD file:9b55d3d522028967302e5d3e4ff8f137867cafb44dde60f16cb4164bcf696f8a in / 
# Fri, 18 Mar 2022 00:37:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:10:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:10:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b1039ed94adda6ad2c358e44a4dcb6e55794a5ee68506bea2119c7395e92522f`  
		Last Modified: Fri, 18 Mar 2022 00:39:11 GMT  
		Size: 28.7 MB (28724094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8728d8dc15c76c2a67839b9755498323086446a2de1a879d4375058dfea3ca`  
		Last Modified: Fri, 18 Mar 2022 17:17:08 GMT  
		Size: 3.8 MB (3818549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0c8ad91f4becbc8656c8d445ef1d2d5bb25c41162f6742822fbf8413e86197`  
		Last Modified: Fri, 18 Mar 2022 17:17:08 GMT  
		Size: 3.5 MB (3470306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
