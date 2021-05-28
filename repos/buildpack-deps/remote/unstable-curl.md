## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:01c4d47d90096b37f64400086aeee4108f5433989076c93ae22431c58d2f9bb6
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b2be4953d60e6ae5785916f0c78c84a989753933aebd4b8ea92b09b6fd95f251
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70937819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d70e684fb0a1ef0a8f31f474d7a78cf10b05539d35429f8d45aa079eba006b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:57:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327df9aed8a8e57527a50678726f61121ed7fc1ff1b0c91e4268684ec7631ae7`  
		Last Modified: Wed, 12 May 2021 02:06:06 GMT  
		Size: 5.2 MB (5169357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b16c115b4ba04c02cb68097f3935495074622e8771a76d9f6a8c99d03331f9b`  
		Last Modified: Wed, 12 May 2021 02:06:07 GMT  
		Size: 10.9 MB (10871771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f7ffcac667ce941ddb2b0241b4589e6f7d7b16939fde3be960ba88e006b1ef27
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c69ea9badc09247a28f77bfb685ee9e70389c7872cb34843617bc6781c1fa45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:57:58 GMT
ADD file:74d49eb3680e0d1e7268c77ac09aadc6a9eaca2541a1941d02c05771fce80430 in / 
# Wed, 12 May 2021 00:58:17 GMT
CMD ["bash"]
# Thu, 27 May 2021 19:55:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 19:55:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:992a8499bbce77a1397237914a5f442e2a2d90912c4dcf8d75ced68fa669452a`  
		Last Modified: Wed, 12 May 2021 01:11:33 GMT  
		Size: 52.4 MB (52438763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919c41d940ed14742ec6f26b83d52bccd7dc9e430c1dda8f4e8acdebb898ff0f`  
		Last Modified: Thu, 27 May 2021 20:06:51 GMT  
		Size: 5.1 MB (5074040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37054668f2f5a38fbe90534d3d0080b9438fb37e6c74493f206211677ac7fe91`  
		Last Modified: Thu, 27 May 2021 20:06:51 GMT  
		Size: 10.6 MB (10571286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aa4541f5eb37294430be021d950c3cdcef27e2d17dbdc7d3b862decbe23d29dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65249957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395ce60024f252a9133d1e8c5e7d55bd9090355a2230f344277d7a24fe0de771`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:08:03 GMT
ADD file:45a139d5ba2871d3a6f990263a8fdb68998d0e072f5c70f796581383ed107962 in / 
# Wed, 12 May 2021 01:08:13 GMT
CMD ["bash"]
# Thu, 27 May 2021 00:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:42:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:187ecf03b42c9078bbaf7c041564e40178e23f795d23634e11536955cfc64143`  
		Last Modified: Wed, 12 May 2021 01:20:07 GMT  
		Size: 50.1 MB (50098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246453820c5b02c5c8b00dc0dde6bfb94015029c6b8005d49ade59af59c0f9f`  
		Last Modified: Thu, 27 May 2021 01:04:58 GMT  
		Size: 4.9 MB (4935074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9c0bc52453d252747af83975a8f1a58fe5bf2a18c4d879befd805239279f6`  
		Last Modified: Thu, 27 May 2021 01:04:58 GMT  
		Size: 10.2 MB (10216618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b5e32f2bff3e8a14ba12e3e3cdc499a3880e9fb982a973dd0f0300592ba795a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69610181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6192c8f165cf8b752639284bcd0b8197c31141fe7355d5b2111abd03f18516ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:54:16 GMT
ADD file:bffb08485a063deee6d89343a52bf604c1b25c42687e69b289d304c56a35e425 in / 
# Wed, 12 May 2021 00:54:20 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:53:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:187d6bdc2d3198067fb9a19db77a105ae346c5a0de7d9892597e87e77c9d4b2b`  
		Last Modified: Wed, 12 May 2021 01:03:04 GMT  
		Size: 53.6 MB (53579726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb9511f69b9636c476ffdf47230c994e46c3f84d8a4fc9a05a7a411e1035368`  
		Last Modified: Thu, 27 May 2021 21:06:36 GMT  
		Size: 5.2 MB (5157768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9f2d66e609db2f12b48e6617317c7a32631908897ed6cd717819467ad6c26`  
		Last Modified: Thu, 27 May 2021 21:06:37 GMT  
		Size: 10.9 MB (10872687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c740d1f98c480540ab3a92c459763ad2cb26c601461fbaca5176e78c105e93d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72463925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818ec8f8eb55fd1e850795b093b60e30f9a09bf258f833b475f39de14d0a66f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:40:40 GMT
ADD file:d1e0da16153884c1e8fed94b01ed7a0d6215598889cf4b3ecda3e4e8e01a8a73 in / 
# Wed, 12 May 2021 00:40:41 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:11:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1831ab5654d838d70f399ab69140b583b6195b99074487f0f45c8b5e2391a70`  
		Last Modified: Wed, 12 May 2021 00:47:50 GMT  
		Size: 55.9 MB (55915170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aa5558f76b4b2d18bec73cdedd5fada6bf73f54d0205204e99072673252113`  
		Last Modified: Wed, 12 May 2021 01:19:30 GMT  
		Size: 5.3 MB (5298708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46130a767ef67e909c93d812e14d36740b2d6673db70121b3239657bf7bf4467`  
		Last Modified: Wed, 12 May 2021 01:19:30 GMT  
		Size: 11.3 MB (11250047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:da0373807492bb0020dd62f73f520ecef947dfcd1b3f370c0e8595b3e01ba367
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69156990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d8d1552adc8b359cf9b29c1dcd537a68c602b125b0516f057419a247d4396c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:10:15 GMT
ADD file:dca45bb65ee8f7144352f7ac752f805807e971fc676ede954cc095be23566bf7 in / 
# Wed, 12 May 2021 01:10:16 GMT
CMD ["bash"]
# Wed, 12 May 2021 02:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 02:02:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:02e79e4ee7225612ac3aad55b918cb4257f8e4ea2821e093d61ce58205474706`  
		Last Modified: Wed, 12 May 2021 01:17:23 GMT  
		Size: 53.2 MB (53155797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0b63156a44114e717b4b43275afc2af76c4643abc5ccd5f74eb95f7154772c`  
		Last Modified: Wed, 12 May 2021 02:13:13 GMT  
		Size: 5.1 MB (5128666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b331baf926199e9584576eb92ab16ebc86d42b9f2840844dfe1a47f4a77ca98`  
		Last Modified: Wed, 12 May 2021 02:13:15 GMT  
		Size: 10.9 MB (10872527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5bea0a3b2478d8978d8fa28665784a09e4570984b64528ea567064cb30f2def4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75844547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd34a72ec6c17f841cfde8f042deba341c4dce2d622daa9b10ceb530bb5f509c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:35:19 GMT
ADD file:7d2dad47f7990dd0f8ed0b034505aa9c7d8afbd94956f80bb57feccf6f7e15fc in / 
# Wed, 12 May 2021 01:35:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 04:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 04:02:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec00b4432728c9f962251efa3d91b6e0339e74ff656fbaad7adad52ce998ea8c`  
		Last Modified: Wed, 12 May 2021 01:45:35 GMT  
		Size: 58.8 MB (58798847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785fbf7f2f224053db3ca18ebfb195a650ed240333b2b7bc423c9a3190693e63`  
		Last Modified: Wed, 12 May 2021 04:22:23 GMT  
		Size: 5.4 MB (5419993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbba1e29d2e9ae70bab4c22a5dd913b1657725f350d6f9c4130d0f30ddc06ba`  
		Last Modified: Wed, 12 May 2021 04:22:26 GMT  
		Size: 11.6 MB (11625707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4749a399c6319688a95603642b01662e0bace242c22e150956d2ea739f2f8074
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69097527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668f7d17e60fdf765c72bb99f7db13f8fab3275c4750be5cf45e3e79ecd73dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:43:58 GMT
ADD file:22b27fbf0808244bac39e39b8239caa784e78a6b5682c7978c1cb4fac0813a67 in / 
# Wed, 12 May 2021 00:44:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 02:28:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 02:28:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:55e7e62594640e8831f8e39a7fe34cbb94c1ebfb345106b49c32b7d6c7e81eae`  
		Last Modified: Wed, 12 May 2021 00:48:17 GMT  
		Size: 53.2 MB (53183650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8529932d914624dabe07c03bc600a762580bed8457dbe8571680979ad85b69`  
		Last Modified: Wed, 12 May 2021 02:35:38 GMT  
		Size: 5.2 MB (5151016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a75f6cba4036a878c0379562599e814a8859cb2041c9de51c09b79bbed27a0`  
		Last Modified: Wed, 12 May 2021 02:35:39 GMT  
		Size: 10.8 MB (10762861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
