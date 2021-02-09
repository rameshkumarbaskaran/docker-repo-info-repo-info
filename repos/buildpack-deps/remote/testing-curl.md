## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:5b111ba91623c118030092ea5b64e006c0921193a1242545a24d1a3fc71a4474
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c3b2fa775aa81299b26a50864a0317229aadcbd87fae72a73c00c83d95cb35e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72190361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1e8d15464b6d5d487b9593c0f5787e40a8b580ae69f361a093b610bfc26639`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:09 GMT
ADD file:730ef8e3327df644cd47994a561a489bfcce5da8103cc8eb34e67321a36df2ba in / 
# Tue, 12 Jan 2021 00:32:09 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:55:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b802c2c29a7757c7475a0b343a18a46b6b27dde9e3fb6b4db61c68ea197b51d2`  
		Last Modified: Tue, 12 Jan 2021 00:38:04 GMT  
		Size: 53.6 MB (53566443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd06bfac0a19b28c6511794acccc260657d53a299701a82ec9fcafe465089350`  
		Last Modified: Tue, 12 Jan 2021 04:04:36 GMT  
		Size: 8.0 MB (7974792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d97704dcad5e05944cbac93df8fdf452cb71e698fd44004184391a44e8787c`  
		Last Modified: Tue, 12 Jan 2021 04:04:36 GMT  
		Size: 10.6 MB (10649126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ef4a78e0edd7dc58af8c0f6af9ed32782517017e87e1d22600d1bb39457d09bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67664516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328bbeac69bf98bf2f18faf052686d3d9dc2e101ce0ad3c5ccd08b33c5e0de6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:49:05 GMT
ADD file:e692f14c1c4483cbc88d3f2b2b98df48a5589bdf417d84c2dd9dbb7388ad079b in / 
# Tue, 09 Feb 2021 02:49:07 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:da2c3be8f08cfd7ddd509966bb4655b1f7c74b4eaa31a7ab733c50e91684f29c`  
		Last Modified: Tue, 09 Feb 2021 02:58:02 GMT  
		Size: 52.3 MB (52282753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9638f6c6794cf8abb357179d6515914ce152a277d089f8baec5e2553acf260`  
		Last Modified: Tue, 09 Feb 2021 03:38:28 GMT  
		Size: 5.1 MB (5054036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9f24461ae5121b4bee6d238f5d67ac3f026a1264614cf4428418453a0cfb5a`  
		Last Modified: Tue, 09 Feb 2021 03:38:30 GMT  
		Size: 10.3 MB (10327727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a6eb0fadb0bef5514f4f004575e1216dabe7f7d926cd42dacae124aeb512ccd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66399716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91263701c62ae3a86f4732fc1a5c5feb04184781eda4728fb624f30c788d752d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Jan 2021 23:59:52 GMT
ADD file:ad9ce4dd05291eba636daae5f0b9de510927734ac26dcca6940d93e88b5c5330 in / 
# Mon, 11 Jan 2021 23:59:54 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:11:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4ecb0a075e68a9a1a4b7394123b05b2811afa9bc0a23170e2e6c42d5ee19a7ac`  
		Last Modified: Tue, 12 Jan 2021 00:09:56 GMT  
		Size: 49.2 MB (49159573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea32ec53c55b5a19d9fb093241be9ba6e2fe2fd55963111e57d39b0973f01c`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 7.3 MB (7265094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b285ad78deb9119d75d41a2decc62fd9676078225d860eec32d20835fa7fb`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 10.0 MB (9975049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:43d4736915d4b66b791ef4dff3d31645e20816250f5d18a3488cb6a6d678a701
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70923298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f4fd9f3dd5c3e2442efc4b43b90be7e813074e1ce15a875ce5ae7d95b235ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:49 GMT
ADD file:0700c58361c6ae34d399d7ca2a5a6f509980a496c07d319f7455d86b483e7f25 in / 
# Tue, 12 Jan 2021 00:39:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:20:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1e62204d5e176f9e5ef453b346203f7bda9e22ed810a0a4e2c14548d7cc3afe`  
		Last Modified: Tue, 12 Jan 2021 00:50:17 GMT  
		Size: 52.4 MB (52428437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f37b86a934fe39fb5aebaff30977af7d0075b2eeb06b1b794582ae2566dff1`  
		Last Modified: Tue, 12 Jan 2021 01:36:53 GMT  
		Size: 7.8 MB (7840062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908ecaa573834d3855dd61a0aabaf6565245ab200624d87774802a93f1b2dea`  
		Last Modified: Tue, 12 Jan 2021 01:36:54 GMT  
		Size: 10.7 MB (10654799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64ca29eb24941f11f069f64cfc3cdf81c29feb55cdbca38f56898ef361c8a67a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72033157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0eeb003ce09741c74158df693152c523161c63494edc334b1e43adb3974d1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:01 GMT
ADD file:f81099d47b3f99bd08895e4a96fb89eec618d9d0e6c9c8b2fb34681259f340d5 in / 
# Tue, 09 Feb 2021 02:39:02 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:07:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e734eb27dd94c1f3c88a6f32899a659ba2861df7282687c7b9c90f8df744b794`  
		Last Modified: Tue, 09 Feb 2021 02:44:51 GMT  
		Size: 55.7 MB (55737065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e825922dd50d020f9bf23f62b411455511e3368cce25b3304525c231209ec605`  
		Last Modified: Tue, 09 Feb 2021 03:18:46 GMT  
		Size: 5.3 MB (5271393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c92fbb51c2a913e1648e9cfa5323f95e95123462fef6d2370963c8b8c23052`  
		Last Modified: Tue, 09 Feb 2021 03:18:47 GMT  
		Size: 11.0 MB (11024699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae3960e65ddaa86d1d494e5b47f6ea7a197a80903c9ffbebcf03d002e0bcc8e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70414851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5560db536fa1a7b44a1c4f9c4ac634401272c0293aa958e468793c1aa8e7ca2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:15:12 GMT
ADD file:171276d9060030f06df201450c4356d6449f4c6a905d02db7f2371f7ed26b34d in / 
# Tue, 12 Jan 2021 01:15:13 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:45:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cdc62d8dca2f8e7c324fa9f4efc40193ada4c98be9ca6b3f1388ad903e4bd5d9`  
		Last Modified: Tue, 12 Jan 2021 01:20:56 GMT  
		Size: 52.3 MB (52264790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b87fc90acd9bd7359cfb81de768ce7f4cdc0821db3ed523142fe855433832`  
		Last Modified: Tue, 12 Jan 2021 01:58:49 GMT  
		Size: 7.5 MB (7492735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6084ef3498948096f602b4aac1a0fb7a2dbaa7d5d751897ddec139d2cebb08f`  
		Last Modified: Tue, 12 Jan 2021 01:58:51 GMT  
		Size: 10.7 MB (10657326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:395e3354a94259806ac798908af6dc02791e1f6eb0f555f0f36e2608ead4cff2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77415262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53a0af5f4fa4668472028f5f823c4da07c357e467f66dbe2cbaa4a04a20fb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:23:03 GMT
ADD file:840490bff9a0b2cb1e20599d893c1160f6884327f51294479567e5d43f91b885 in / 
# Tue, 12 Jan 2021 00:23:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:39:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9d21ce86f5496c36ba2ba289acb977a3b160c6c56fb257c10e3adb8b55164a16`  
		Last Modified: Tue, 12 Jan 2021 00:32:24 GMT  
		Size: 57.6 MB (57562164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d42b61558772eb59064c0ebad8029e0e7524bf865c29218b048871cd3e43fe7`  
		Last Modified: Tue, 12 Jan 2021 02:37:14 GMT  
		Size: 8.4 MB (8431230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663cfe2e2cfc28477e509f0e7aaffd4159d2f37157b32a7327bb6f43a7508ac4`  
		Last Modified: Tue, 12 Jan 2021 02:37:17 GMT  
		Size: 11.4 MB (11421868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:29a8549158e40c78622e677b7b2ce4fec56c5632ac5cc3c51a53c87f3d9fe406
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68652909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27504c4808fe1e16b056765946aef4a6cc628eac23bf38aed8228df2fff735e1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:32 GMT
ADD file:b29f05e744766860cbed836c9527b8ec4e72570959bb61a8aa0e5c363cb72484 in / 
# Tue, 09 Feb 2021 02:41:35 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:03:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:03:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6eee01c120872bf1700180eee1b04681a66f946d188f352a1a7d516d703e4a66`  
		Last Modified: Tue, 09 Feb 2021 02:44:42 GMT  
		Size: 53.0 MB (53006960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d2f6f124d0127ebcdbee7e40a00127640a914d79503aaef238ab4afe12cf36`  
		Last Modified: Tue, 09 Feb 2021 03:10:53 GMT  
		Size: 5.1 MB (5127719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216ed6227ef8df582c34143415b588c1ed64bb3ed322108f9c67d4318a5e6b2`  
		Last Modified: Tue, 09 Feb 2021 03:10:54 GMT  
		Size: 10.5 MB (10518230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
