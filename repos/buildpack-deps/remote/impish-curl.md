## `buildpack-deps:impish-curl`

```console
$ docker pull buildpack-deps@sha256:b1996441b42915fa320ee802ffb48e8174e4cd96d6c81f1299ca84fbe2b3bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:585099f987fa801207134792d9021931665cdd039b8d629bb2ce1507148bfea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37632053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad70cc966de3c39b393791d82db65f8361bea091f8b1dfc56c1cc0b8dcb4cdc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:40 GMT
ADD file:0255a38a25ff74df5705cfa360847fd81f98cc513707203d1e54a75263f54a76 in / 
# Thu, 03 Mar 2022 20:19:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:53:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec78bc49f256d7c26847ea612014b0bfd18cefe448e2b8e327512c6839fdba84`  
		Last Modified: Thu, 03 Mar 2022 20:21:02 GMT  
		Size: 30.4 MB (30385738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac486f3e51c4ec586a48b678184f79c60cc82e142eb10b4eefb4f894a0c8fa87`  
		Last Modified: Thu, 03 Mar 2022 21:06:32 GMT  
		Size: 3.7 MB (3694199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7dcc7b569cc2b1f8acc8b2ceeb11a411d6c50ffe47bfc0b5b2066864e7ed5d`  
		Last Modified: Thu, 03 Mar 2022 21:06:31 GMT  
		Size: 3.6 MB (3552116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d496c2e875c7a97cf76c4866538c9246eca8340af0a2b8937e11230b517f0783
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34108977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6618e4e04ce8382c5a633dc3d4d0a5ab6cee53071d11ec4e524755e49160bbcf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:55 GMT
ADD file:2147b6b5f5a6085917d41d8d2c1cace254f6f07b78f75973d696c4aadc615c7e in / 
# Thu, 03 Mar 2022 21:21:55 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:22:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0e5117981c2b00f6b01a0a1aca7c0fc638269b9372a736c2f4e60f0ee26f1c88`  
		Last Modified: Thu, 03 Mar 2022 21:25:44 GMT  
		Size: 26.9 MB (26921937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f27cd7b6a3b3adf03f7c99abb087586c307ea8a6822f834cab8840e832a48`  
		Last Modified: Fri, 04 Mar 2022 03:40:09 GMT  
		Size: 3.4 MB (3443736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166ccda40e86aecd84ebc63263f1e0fbf366905e989217e8e90ab8e42845d855`  
		Last Modified: Fri, 04 Mar 2022 03:40:09 GMT  
		Size: 3.7 MB (3743304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2d61871de7613cfd92b6b2ea5be8781f147b9275bc4d70590f313ac323a373d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36038760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9d7dfe256ff8be619c4f914ea3ec4bb91f667783dbbc6b60ebfbde89a7c4e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:11 GMT
ADD file:0e8c3ab0e6e7f15d32d0e43c17409e1ad9e4c77cb87b27edcb23fd8bbd941784 in / 
# Thu, 03 Mar 2022 19:41:12 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:10:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:10:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:070b8fff765c544371e1499a46e470f8c2eeb6f493d1e9949af6b068f1208ad8`  
		Last Modified: Thu, 03 Mar 2022 19:42:58 GMT  
		Size: 29.0 MB (29031972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bb6800b180c2bbd9c0d917ea78669aa5e7110362527fc96692bdb2cd314ffa`  
		Last Modified: Thu, 03 Mar 2022 20:18:18 GMT  
		Size: 3.7 MB (3679015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd2a7b702ea3cee495ba3e01196c92f87bcd77f372d995d2ad1c555947e9da`  
		Last Modified: Thu, 03 Mar 2022 20:18:17 GMT  
		Size: 3.3 MB (3327773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0dee8c335f26e675eca116966e04482a45cd582ebd2a33f991217ceef9943f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44565955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfc56de675acadc30a81ef69d5624e827083aec12e90b9cf4bc89f41ba93df8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:54 GMT
ADD file:c9dbe94a6e712a5b1a894d57c1396be96b5bd702e90b77b82817ce85618dadcb in / 
# Thu, 03 Mar 2022 20:29:04 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0c4c4e967fa8621c96984594294f639a4d7ec13235867cbd56a506b4ef96bf1`  
		Last Modified: Thu, 03 Mar 2022 20:35:37 GMT  
		Size: 36.2 MB (36175818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8dd918329f318acaa93d44e882d2d310d61f08741b32bf697e381e348af61b`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.1 MB (4147822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f180d1cc1b110578ee29533ee2466d939fc44bb802f1c74ea0241c95d3e02`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.2 MB (4242315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6a3fea4190bf5b4186d98d8f53e9bb9137bfd288c4e2c2c961c3ec0b61d4bc2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34509275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcfbcfb748e61ad022fb5f9c10cfe2fb724e3c7f86c6089fe0e66e6b1fb091f4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:17:50 GMT
ADD file:e036bf8d2d9837df0754ed0751c2cfd386039c558c517121d3a048a6a37b7afd in / 
# Thu, 03 Mar 2022 20:17:51 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9f00725c1dfb59f0dc5edf593a8b3a65a79cb2106fd1dfb0492c29b0d3d04a6a`  
		Last Modified: Thu, 03 Mar 2022 20:36:05 GMT  
		Size: 27.2 MB (27214379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149e59e6c41692bd9b82ac05ccf0b72418a256938af0b0286e7e720b6306ffd2`  
		Last Modified: Thu, 03 Mar 2022 21:53:23 GMT  
		Size: 3.5 MB (3490700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c849cddebc546bc99d5cc608c1a923dc6423d55265f9d59ec59e26220ccb015`  
		Last Modified: Thu, 03 Mar 2022 21:53:21 GMT  
		Size: 3.8 MB (3804196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:84b5d4e7a1dc522d4c32a7ff36f4865ba02cee1869668037fb48c3878963bd4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38251300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff7b21e9708cbe6b5afc44ac8f1d955e14ae71c47b936c87e5431a5680310ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:42:01 GMT
ADD file:e150af68d3db546783a6fafa964d1b9264cb1b35930b07255ce083fa0c40e532 in / 
# Thu, 03 Mar 2022 19:42:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:36:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e0cf59e92c5acec5ae595918f7a30d60c44156b11926f39465f58e2132619a47`  
		Last Modified: Thu, 03 Mar 2022 19:43:36 GMT  
		Size: 30.5 MB (30524528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7871093b66fa67764e2403a711a69a008b0941e41ea3b9edb6b89473ad18a0`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 3.8 MB (3763377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3fc096c211db0aeef7379615bb3126fc4a81163cc8fc1c0b54d1ada0869b3e`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 4.0 MB (3963395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
