## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:9b58912204f1bff60e9a4f1a585023d9f6c1b856796d56f4ad1db9999d497ecb
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b677e93df12ff82852ec41168deb90d09f9f36cf6b0190b4ee4133a26613a7ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129575885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dbcc9e957ac58b3583e5e1a961760f078620d6a7d3944203d3fc19861f6fbc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:41 GMT
ADD file:388f29164844b8493d30bf1feffd1158559ab161886928f977604c10f983a704 in / 
# Wed, 22 Jul 2020 02:05:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:09:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:10:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:babaea2ea26ef0e3e4a90ecc928d26bf25d699e1dcba843f16b8a2f0a153b3d7`  
		Last Modified: Wed, 22 Jul 2020 02:11:28 GMT  
		Size: 52.3 MB (52340330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a37a5f4c4c2303f8d9f818b910d8f9caefdb8cf414a4189c131fe87eac26c2d`  
		Last Modified: Wed, 22 Jul 2020 03:18:23 GMT  
		Size: 7.9 MB (7921724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a136692b9cb363269d4efa1edc43bf0b539b0495b6ab5f8229f02319829642`  
		Last Modified: Wed, 22 Jul 2020 03:18:24 GMT  
		Size: 10.6 MB (10580682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044462b11abaf8b753d1589c7b6b7d8c20479da7e1c06538ea604786fbbbaa62`  
		Last Modified: Wed, 22 Jul 2020 03:18:41 GMT  
		Size: 58.7 MB (58733149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ca529eb83e87ee195ddac283e1fd746281621f827124760c1889bd939570cd8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124381214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7012fbc78ae2025473372b02afeafbf918935fc191f68a2a572b6d02f550c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:19:33 GMT
ADD file:966adedb56b8840e71e14255f1e10c11506897b861f32a0c8c84c32338edea04 in / 
# Tue, 04 Aug 2020 03:19:44 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:24:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:24:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 06:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70fc41871a830209ccc29805b1bb08b4058beb41df471ae13bc23555229a9623`  
		Last Modified: Tue, 04 Aug 2020 03:37:01 GMT  
		Size: 50.3 MB (50310118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042826fa49924c4933b5f443c67da73885272c029983f30a8e5a154ae5b2ba7`  
		Last Modified: Tue, 04 Aug 2020 06:39:59 GMT  
		Size: 7.5 MB (7501462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f2d1c9e043d778892369b2ac4ba55c261e45346581518d8e9c0923f580979`  
		Last Modified: Tue, 04 Aug 2020 06:39:59 GMT  
		Size: 10.3 MB (10267096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1e363591d4c61017b4adf9fc9d4b3da3938064ff6fbb809e08a84bf5049cec`  
		Last Modified: Tue, 04 Aug 2020 06:40:32 GMT  
		Size: 56.3 MB (56302538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:00bdde0413f57d556a4e3c18e22352cf9dffb46e63e00c58292e78c147e8ff12
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119116563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5141699dd6e5bc3d4fc1139d0688ec931b82fd2806ef67f4e8b6077ba4192dc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:59:26 GMT
ADD file:5793438e4679788bcbcd7ff2adcfe8f0c31bb4ceca63088d7c74a20cac1e87b8 in / 
# Tue, 04 Aug 2020 04:59:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:08:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:09:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:10:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ebc2f87ea858cf67ec5ea8f8fcd77fa8fefcd9b35b71d1b3efa355f8289ce59`  
		Last Modified: Tue, 04 Aug 2020 05:07:30 GMT  
		Size: 48.1 MB (48082910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76657e19ac1e0b31daaf79a3e351dad82e57e1e9714d8bcb5ca885c77b1150d`  
		Last Modified: Tue, 04 Aug 2020 08:29:01 GMT  
		Size: 7.2 MB (7243562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227bb50b47817c708c54d7d565ccfc1a6a7f89fdf3edf9cb85c81453f41011e2`  
		Last Modified: Tue, 04 Aug 2020 08:29:01 GMT  
		Size: 9.9 MB (9915847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f083ffc50f274a9b7bab4204c81cb5d08c3488fdec1a235c7acd3d6293a1702a`  
		Last Modified: Tue, 04 Aug 2020 08:29:29 GMT  
		Size: 53.9 MB (53874244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d967ce10aaead3ebf6acd885954ab9a86cf80edeb379d9e0ba00ea8083a3d75d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128016452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12b3a4a76f67340c19269f59d12dd7ca041a7a1dbd27bfd35018e1bf84a77a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:14 GMT
ADD file:0f4a1ab6b889d98f711b241dde31787e633494e233067fe98dce73de73c2d7f3 in / 
# Wed, 22 Jul 2020 00:42:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3af651ddf153ddf8519b20c192d158afb60045252366ddc81e15c938b792982e`  
		Last Modified: Wed, 22 Jul 2020 00:48:41 GMT  
		Size: 50.7 MB (50699554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb2a684c92e31711be180ca45ac19643d88c12a51b2ffb58b6f120bc5ded2`  
		Last Modified: Wed, 22 Jul 2020 01:37:00 GMT  
		Size: 7.8 MB (7796374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdf66380a30dc7828150f57df61c812d1fd653b195e8f5d57dcfb885adedbf`  
		Last Modified: Wed, 22 Jul 2020 01:37:01 GMT  
		Size: 10.6 MB (10588039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74e3c1552e3888e748a1827b0e10da06ab4a4d5d05b69a591c812b9a0a1dcee`  
		Last Modified: Wed, 22 Jul 2020 01:37:26 GMT  
		Size: 58.9 MB (58932485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d8ee149c206668335140752ad317f3113df935235b87b1737f10063988cefee8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133450673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3863f9103f6d6f3532685dc0e1d9cb6e5081735f658caaf5d9ad432eae4e4b68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:39:04 GMT
ADD file:545a4c28d2d65f9f31d6deed3b22ae80dcdf0f0ba234b36acb715ebf6da67f3f in / 
# Tue, 04 Aug 2020 03:39:05 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:19:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:19:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5671e8963d62284adafd28133509ee2239373c96d0091ce2b4491327cac9724f`  
		Last Modified: Tue, 04 Aug 2020 03:44:13 GMT  
		Size: 53.5 MB (53490363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58173079354050a764e0b7ab86cb86890a027949b6c49f2f6e431042520f5793`  
		Last Modified: Tue, 04 Aug 2020 08:28:46 GMT  
		Size: 8.1 MB (8099063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5b5148c590d93c505260dbab5cecf462a0afd80a0aead458ebbc0ca4cbf438`  
		Last Modified: Tue, 04 Aug 2020 08:28:46 GMT  
		Size: 11.0 MB (10960412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f5cb4e332f3b1109c6672be060a7766e25652f77917b2bd99d249c2dc27e`  
		Last Modified: Tue, 04 Aug 2020 08:29:08 GMT  
		Size: 60.9 MB (60900835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59022f075cf83c03cd393ee42b9d6d29a63d72f3635aa8c71ef26f9b03622745
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125229559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058e16b323d328e897a506d65d65fc23b84c1f07e9c3a022fab9d21719576761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:10:23 GMT
ADD file:ba027e751512c2bd75301e89e6e4ff2f37ba0d5a4dc18785ef0805c0c44217bc in / 
# Wed, 22 Jul 2020 01:10:24 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:40:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1d6004a331270728a8745881ac080835166c19dd8097eeccdb751f6118875fd`  
		Last Modified: Wed, 22 Jul 2020 01:17:34 GMT  
		Size: 51.1 MB (51078870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fc8ab221636edeabd2df88a6e60355b1cd646986a8adb8b6e026bdb27a37a6`  
		Last Modified: Wed, 22 Jul 2020 10:50:36 GMT  
		Size: 7.5 MB (7450064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab2cfa46cbc90566aaca1e1931fc9c28d4dacc60e71e68bc28c5e245dc5a178`  
		Last Modified: Wed, 22 Jul 2020 10:50:37 GMT  
		Size: 10.6 MB (10598947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2dec4880e8fef552766207810870fe577d2c2340629a099ca64ee775cdbdc3`  
		Last Modified: Wed, 22 Jul 2020 10:51:31 GMT  
		Size: 56.1 MB (56101678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:42f062a951f5ddf91308f24a7d2e21ce07fc023385576717d4140e86f9961e69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140485459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8035a099f7e91d7379ee7efb65722b7fd57e5a4e8ead4f53ecae9b4d29106`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:56 GMT
ADD file:4f9206295fed0198f64e3e8588d30592afb355ad315b7f02a90d92274b37766a in / 
# Tue, 04 Aug 2020 04:46:03 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:25:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:26:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:28:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54ff323e52b64530253b6d180607b58565d781a9b132031a9baec3e1577690ab`  
		Last Modified: Tue, 04 Aug 2020 04:53:50 GMT  
		Size: 56.2 MB (56196736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6163322bc0beea20fbb00969be62fd8e2c8790b205e246ff0b8d2a3b72ed82`  
		Last Modified: Tue, 04 Aug 2020 07:46:38 GMT  
		Size: 8.3 MB (8347727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae8dbc9e7891e1d54106baaa34d375e35b66be62a672cd47f7d6388f7ed7797`  
		Last Modified: Tue, 04 Aug 2020 07:46:39 GMT  
		Size: 11.3 MB (11327086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123657860e3a0579d09f7f5f2bed55b40d18ab151ca05653ce1c874ea4be1b9a`  
		Last Modified: Tue, 04 Aug 2020 07:47:10 GMT  
		Size: 64.6 MB (64613910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:84270f0b085d38d2474da2e0bf161bf23b139c226dccc22c179641d66bcf5ff8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127162825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ec46934dfdb3adee4d568713f83345892418aef419af62d98bf3436836bfe8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:26 GMT
ADD file:a96b6121a19d104791604cd0cd10ee066e9d0f56abcc8f3f9cc1cfa691f2c4eb in / 
# Tue, 04 Aug 2020 01:17:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:24:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:24:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:24:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1776f15db22f5bcf0f222cdcea18411e8904b4ebbb37ce537b90d8cea466e2cf`  
		Last Modified: Tue, 04 Aug 2020 01:20:17 GMT  
		Size: 51.0 MB (50989676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f212bdfa67a70fdb2386f3fb1144782ba98880a13323180bd4a44055bb72ad5`  
		Last Modified: Tue, 04 Aug 2020 02:29:04 GMT  
		Size: 7.6 MB (7590154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f4dbf2b7c1eaaff8920fcd760496fead3e0e754c6b5a9d4122863158fba63`  
		Last Modified: Tue, 04 Aug 2020 02:29:04 GMT  
		Size: 10.5 MB (10456390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97873f50a31c377671799e4bea24e8ea9d922f2c499e800e0808c1f3edceaf9`  
		Last Modified: Tue, 04 Aug 2020 02:29:22 GMT  
		Size: 58.1 MB (58126605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
