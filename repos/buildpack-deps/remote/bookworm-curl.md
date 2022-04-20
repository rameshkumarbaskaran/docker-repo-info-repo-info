## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:c78f9ac2152ea760a3407571a6ba4a47003cf11d01e69e2aa0d8af14d39572f2
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fa86b7c82d8b945bb5967ebf8986a91a4b9cd6e4f4fb4e9082e4267b7f234652
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71711235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2de7d5b7c2db26a6decf2bd01b939710eb45678d2bab66417af6226fd91c183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:42:54 GMT
ADD file:b5180fc4d45b984afa69f3cdfa95980bcdfd76d75f704f74f1aa60e416272f1a in / 
# Wed, 20 Apr 2022 04:42:54 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:56:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8cb01d170a54a4c7fd7c1969e79df0a453468ebabfe1d860b863f7a3b6fbbc2f`  
		Last Modified: Wed, 20 Apr 2022 04:47:18 GMT  
		Size: 55.6 MB (55578729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec411cc74e7329b4aa762298d902d14025f16214d6dfccffc28adffa29c655c`  
		Last Modified: Wed, 20 Apr 2022 07:04:37 GMT  
		Size: 5.2 MB (5208374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3518a73a45d857ec3136592d439326badcede35952ad723c33e4148b5e83d9`  
		Last Modified: Wed, 20 Apr 2022 07:04:37 GMT  
		Size: 10.9 MB (10924132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:85a7f439242c91eb3bc5dba01f9b492699c4180e1ffbea058851805c4725a761
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68703710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891b3d6a7f1fbc4f1444276f0037dd8b04a34eca2b8c251546a9876ae8472850`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:15:05 GMT
ADD file:e283a0d8ab69b94018679c485439a2b5700bcbd73218180b0a334a00df340093 in / 
# Wed, 20 Apr 2022 07:15:06 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:35:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e7b4944a983e7a423568be713ae200d96e80ca1893c45b7758ec97be00ab710b`  
		Last Modified: Wed, 20 Apr 2022 07:30:20 GMT  
		Size: 53.0 MB (53001097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b73ce869fcfbdc3ffaeaa0d7d3b07f9fb196e529df28d7cce0d9976f8e0999`  
		Last Modified: Wed, 20 Apr 2022 12:58:01 GMT  
		Size: 5.1 MB (5105021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98c07b037b55f8ee9d1521c9f7f55cce527352418e84f9bb81e54017e02f8e9`  
		Last Modified: Wed, 20 Apr 2022 12:58:03 GMT  
		Size: 10.6 MB (10597592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98bf0c477654788adee55a6f651bb90254cfa7e4c1ce49e1edafd85174bd3819
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65827259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e865e0dd416d284b20c8f91c46102ff255b9493c980388a355041da1c1c4df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:25:33 GMT
ADD file:b489c04ffff2353f6ceea0c110a1e81cc311de6662b48af844e74c82fc7b8155 in / 
# Wed, 20 Apr 2022 13:25:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 20:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:03:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:092c836e0e284efdd221da0378b0c96d6671f0ecf169a2e2a6c40b20606d657b`  
		Last Modified: Wed, 20 Apr 2022 13:41:43 GMT  
		Size: 50.6 MB (50620332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21007c9d3968655d957f95b54e8f8146e52f5176047137db4f58682503128bc2`  
		Last Modified: Wed, 20 Apr 2022 20:28:09 GMT  
		Size: 5.0 MB (4962319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6b7a29ee5e509dfb034f594efea5050a9c371e2d0927e6e21c6922c24385f`  
		Last Modified: Wed, 20 Apr 2022 20:28:10 GMT  
		Size: 10.2 MB (10244608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3bb6958ce79bf82681d3a17f92feac08248a1bede7fa6ba3c1caa323539d8d3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70379631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ccc8c136a103599fae1c7ed173981868ff7abe2554eb26d9d682bb407af77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:28:29 GMT
ADD file:23397ad30e34521aa2c0881ab09c9c75f58316594a1c14f01cfcb212161c32fc in / 
# Wed, 20 Apr 2022 04:28:30 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:42:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:42:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c6d996fb7c2fde9d95056213e2cc0a2ea025cc86ce1ceeac46b8c51b2d458d84`  
		Last Modified: Wed, 20 Apr 2022 04:34:39 GMT  
		Size: 54.5 MB (54493289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ee691ff28baa681054135ac8fa72e16199a7024e056d33c427338a21e4dc9a`  
		Last Modified: Wed, 20 Apr 2022 06:53:00 GMT  
		Size: 5.2 MB (5195219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b23bcd2aa6bcebcec9157dcb6c0fecb23e91f1255c588550180d6cd7f9fc26`  
		Last Modified: Wed, 20 Apr 2022 06:53:02 GMT  
		Size: 10.7 MB (10691123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c1727f49f415a47ecd0bae0db686733b2dbb2f405354525e8b6c57b058564428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73068044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5475529cfc1d5ec58f538bc927e28de187a0d9418d4cfbf2aae0db2279573a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:36:51 GMT
ADD file:469d404c80a1f5720a0a00e4cd116adfd490349ede3a368fae44c6409add4819 in / 
# Wed, 20 Apr 2022 07:36:52 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:13:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:13:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c3d3d77c2c71a18bcd4eead6143eb6d36f5096a31d00bfdb4cbd88058ba444c8`  
		Last Modified: Wed, 20 Apr 2022 07:43:35 GMT  
		Size: 56.6 MB (56624540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f37953affc719c71f109e570bbb539dc712570c50eafb76adeb6cd853aff96`  
		Last Modified: Wed, 20 Apr 2022 10:26:12 GMT  
		Size: 5.3 MB (5339609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f627a1c0c008ccb7b51d8adfc2441ea6d92182113c32697e7aaba9541bd9197e`  
		Last Modified: Wed, 20 Apr 2022 10:26:12 GMT  
		Size: 11.1 MB (11103895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:962defbea0e0cb26af17eff946a1521b40c94358b14fdd501168a7d348343e4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70134662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cf8881739ad3d127d09e672d5033bad785feabf3c2498a9f32fd71e280c217`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:40:39 GMT
ADD file:88e75745fdbfd0784c1c18134a0a52a5534df18201a6f49555a5c618b4531804 in / 
# Tue, 29 Mar 2022 07:40:44 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 08:17:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bdc3f4c024aea887030bcf477ee808da6aa3e6683fb111845d94ab4f2480ff24`  
		Last Modified: Tue, 29 Mar 2022 07:50:58 GMT  
		Size: 54.2 MB (54240334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e94f68f0d96094b4bd1aa9ba6f4465ec7d6879ed28f910b949ffb165eef3fe`  
		Last Modified: Tue, 29 Mar 2022 08:54:21 GMT  
		Size: 5.2 MB (5221857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd581c56a027feec68bb7a881cac731bca045297cd76398414512c34351a063d`  
		Last Modified: Tue, 29 Mar 2022 08:54:24 GMT  
		Size: 10.7 MB (10672471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:077d06a1abf8e23db782092c7852fd24c381de5d5d704977208977b66834db97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77168687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e44dc76766e5d70fde46d839c4b2ea6947fa81d352c1fe6cff92f52eb231113`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 09:44:36 GMT
ADD file:b40661820352e5ff94b93927c06b3375d894c06269350d442169c7a7b3952388 in / 
# Wed, 20 Apr 2022 09:44:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 16:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 16:31:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9f7d9b4a813a5ec1ec0b3475149a2c942961debb65bc15ebf43901246ca6a9a3`  
		Last Modified: Wed, 20 Apr 2022 09:55:28 GMT  
		Size: 60.0 MB (59982654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b685cd9772e83ee1ad7c0caca17d1344e88a0884802d3c467ae1df883e2d420`  
		Last Modified: Wed, 20 Apr 2022 17:22:29 GMT  
		Size: 5.5 MB (5482653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481aea90c025fad74d53ef4647f2c79d6661482c7d09333e65fd573ea4744ce6`  
		Last Modified: Wed, 20 Apr 2022 17:22:34 GMT  
		Size: 11.7 MB (11703380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1d8f4ffaf586812384c733052dda62edc265e5fdcceac3e81a221ea6e7fe5b89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69816564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c809e182bafb8827563555a16ee7d27e657df4a58ba18b65c4e68e56119328`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 08:37:57 GMT
ADD file:dd66488219818707ab57e2b9e87dcec876513326c64a733dcf95396ad5f22cd9 in / 
# Wed, 20 Apr 2022 08:38:03 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 11:09:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:09:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2b24c47356e8597f2e75ec110237cb3350c6d41c44b019ed531f1d9069ab1a82`  
		Last Modified: Wed, 20 Apr 2022 08:48:48 GMT  
		Size: 53.8 MB (53813432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f80f6a4ee41ee80e5063d1d7d86ebb328ffa05ba98de6fe03109fafae44721`  
		Last Modified: Wed, 20 Apr 2022 11:27:14 GMT  
		Size: 5.2 MB (5185393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd7e687f194e7ac60ded4e1bfd0eeacd9d22b2785dbbdf847eafa68e6a0058c`  
		Last Modified: Wed, 20 Apr 2022 11:27:14 GMT  
		Size: 10.8 MB (10817739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
