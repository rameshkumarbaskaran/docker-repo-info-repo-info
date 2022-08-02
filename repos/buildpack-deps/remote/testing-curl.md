## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:5dc6f8588dab6caf2e287042d1017f26e32e626f46f942c7c358ab754f48e73b
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f672cb94a21b691b5622eceee7146ff9d63c09cf9b9a615468cda4982bce031
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73586402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a3576a74b27fbdc9ee30a6d3bcd8a47de0d620783f4f3237a349f712bf5f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:34 GMT
ADD file:e413c7d61ecdc96ab067e1f8bff6ce03c792c94b9d1f54e80cf633052c5d975a in / 
# Tue, 12 Jul 2022 01:19:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7c7a32fcf1e30b18b7a9a032acf892763291bef7159859a35297bf81217bbee4`  
		Last Modified: Tue, 12 Jul 2022 01:23:29 GMT  
		Size: 53.0 MB (53022393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00146b6ba9670f0b5362fb1ea6716d934ae0d1545d85efb6e7d9871f449ed7f`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 9.3 MB (9292245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed5201b04ed0ec80bf5f970e6e10f4e241d58bfbeff69ec15faa4c6a34f01b6`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 11.3 MB (11271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1d1f19c055520a3ede8c9549515730d5fe1d1c4f205e11ddea10991e17b7b9e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71499327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4817e4dd35592e41593c4ed4c1dc3c62de76e8c3aba9378dbc93d5121b3e2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:48:33 GMT
ADD file:f83bd7c88ccdb8f7b53f9072524438c8262a71b297a007c804923fd6d817479b in / 
# Tue, 02 Aug 2022 00:48:33 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:17:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:18:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f721a266d53173a0af0b138649440b41e425660c1bfb8506b479507fa2627c4d`  
		Last Modified: Tue, 02 Aug 2022 00:54:42 GMT  
		Size: 51.8 MB (51812934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6a541c310c2e2f0c838ea71f560b2bf4a91d0e9c4c71ab80c566d34acaae98`  
		Last Modified: Tue, 02 Aug 2022 01:28:50 GMT  
		Size: 8.7 MB (8739729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928c72f00c51da560bfe1136e59212f70544fcc07732cc6b7156db46dbf7d55`  
		Last Modified: Tue, 02 Aug 2022 01:28:49 GMT  
		Size: 10.9 MB (10946664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2db2f6416e9ae679ed401e8a1a940aad1460fd0c2e53573c8a2b815fac9851a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25822c472580d34a2942a83018b9b1d8579d45a3a068797b60fc5fe1e536411`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:57:55 GMT
ADD file:359193f5179bfdc5181bda2e05bd0b22ae4a86c638b0bbf09f289d1727fad222 in / 
# Tue, 02 Aug 2022 00:57:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:45:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:537407bee93780ba0135c6d74e62d8cee8d32e85ab926669d3cc9bedeef28852`  
		Last Modified: Tue, 02 Aug 2022 01:05:20 GMT  
		Size: 49.5 MB (49527674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21e0c1ecdb66b081e679eaee092b97020507b0a7735843a508a74b1ecb86429`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 8.4 MB (8417992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2371236f490dda856391359574a3e2e3ecf9d8d39f77649c8c6839a1846326`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 10.6 MB (10589533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed42332d1c3a5a7ca76529f1e50f807507a6bfa762041b1d570c8cfce77ed006
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73308393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c77fe24743eec785040e635d56987c0001324b2051298fd7d47b6340b0cf5fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:01 GMT
ADD file:66ffd29b395276f108023b4be1a449714b6fb1fcbcaf770debb7ec6910e84294 in / 
# Tue, 02 Aug 2022 00:40:02 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:22:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c76fc726ec0ec853818bf6b42fbe47810086904b89f146d4ccce624e8c5a33e2`  
		Last Modified: Tue, 02 Aug 2022 00:44:53 GMT  
		Size: 53.1 MB (53097492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446351798668b67b250456bd33621fa3f1239a40db1aa52cbae04c3c1524f3b9`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 9.1 MB (9148571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a6b5eb548691ce9ed80e732c56ffc57a9ff5c14103b158596eb92a0508c44c`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 11.1 MB (11062330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d5a3074734b144eb9171a7c0a13db31918976fb0a958d2a9af21c4f5a8aaf4f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74922807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baae06c055d047424b7212c445d1a9a0a46a56436d591009288a551f7bcd6080`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:38:40 GMT
ADD file:f331e5b0e8626bfcbb682d701943586f63db1ff65d9add0d94759ecaeb8c8269 in / 
# Tue, 02 Aug 2022 00:38:41 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f78c3dc38f418186e278713175ef4cfc4bc70d85867d3597da89d03b5b956170`  
		Last Modified: Tue, 02 Aug 2022 00:43:55 GMT  
		Size: 54.0 MB (53974067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d30bb833cd65f6a8dd0078ee5cb794a55e3d1ecfe364e6976104636596e4fd1`  
		Last Modified: Tue, 02 Aug 2022 01:22:56 GMT  
		Size: 9.5 MB (9475285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e544133d2cd6d41cae7bfa63047f55cf4e607b50597b796c9562f4425da665a2`  
		Last Modified: Tue, 02 Aug 2022 01:22:55 GMT  
		Size: 11.5 MB (11473455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2be0993a0496e36806a4e7bf59363cfc6dacfb5c75bc8486937ad4ff0b1adcf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71839292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a166fee9b8076060744a2572524576fb2ec6b80006c078d83b56c39a45652e3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 04:39:09 GMT
ADD file:a4c1c80b05ba336cf2c87e4c90f5bd31ad9a6952b41985b49461741377bdf82f in / 
# Tue, 12 Jul 2022 04:39:13 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:00:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d42ff6e50c127c0849c96192832cf954071e1fe597bc69ae0894999838a3d95b`  
		Last Modified: Tue, 12 Jul 2022 04:49:46 GMT  
		Size: 52.1 MB (52148304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6761aa7c460392eac1c72e9e3d658302ae105a69f107d6b7fb8bce7f988b5b`  
		Last Modified: Tue, 12 Jul 2022 06:37:09 GMT  
		Size: 8.7 MB (8657917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6e4ee7231527a7e9598fb19bb5b34e13789124eaff6a2955f130d363356fb1`  
		Last Modified: Tue, 12 Jul 2022 06:37:09 GMT  
		Size: 11.0 MB (11033071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e6f20ff891bd42d4e3bda4d761fdfd188f7006bb154a6b6ac5fe7801a7ce7e2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79223335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180dc35d74cfa8015f2768034c9fbda6385836b3d638745beeab0b8563a25a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:24:07 GMT
ADD file:ae1b00e1c53ca0bbd56262f1d2cd742362c7a02eed6214e944b4b4762dda64ff in / 
# Tue, 12 Jul 2022 01:24:11 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:28:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8000c6ba1eb02ffb5f03a6b7e7d8f71a864844286f05cb8516ff71014b1cb870`  
		Last Modified: Tue, 12 Jul 2022 01:33:34 GMT  
		Size: 57.2 MB (57237580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa4d5388d97e0872477cb7660fbd3c341738064717f187dcfc90f0b64e8e89`  
		Last Modified: Tue, 26 Jul 2022 23:45:55 GMT  
		Size: 9.9 MB (9902776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05727228be0751bdf9f161f49f4edda690903161ccbf1593b8a4a16062ad8ce7`  
		Last Modified: Tue, 26 Jul 2022 23:45:54 GMT  
		Size: 12.1 MB (12082979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:82f2b8a76d81bbeadbe2ed7a66d543f39061f17eb2dd0f2d9bf574a2316faf2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71633726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401a80e01b8e610b26c270753d3e09f013467fecf6910cccb6f55363aaaba98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:9364324d9e3e24a6e417365a226c42bac5c3c9589b444096a65d5bf539eec127 in / 
# Tue, 02 Aug 2022 00:41:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:07:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1a5bd7c6618b65a5948f8c07805e4109ef4f5aac36711b43d0fabe6f11fe0ec8`  
		Last Modified: Tue, 02 Aug 2022 00:47:13 GMT  
		Size: 51.5 MB (51514530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c61b0b54c9dc1946fb336e5a04c532d39a45e681f19f307f477085013dd8bc`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 9.0 MB (8952435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edc88e19b9b0261e01462a1883dcbc8fd4849c5a80450a4659c246ae5188132`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 11.2 MB (11166761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
