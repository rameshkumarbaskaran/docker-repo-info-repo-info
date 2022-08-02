## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:894df498fdf77064b6f8e2eda31679a5776187791760f506b94a9918eef2cfc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:82fecbfabd7747aebba04397da6a534bef52a02c03d7322b8284c48f99f4c2cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77385592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e11b5950fdf2f45c7b523dc7503177e85f5420fdb3548fcecdef4602ba2d115`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:33 GMT
ADD file:440048faae869c09f5819655d93c479ac0282dace791dc6077f035c8481f45b8 in / 
# Mon, 06 Jun 2022 22:21:33 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 02:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:20:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 07 Jun 2022 02:20:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415d72858c745ad20ae2769e6ba46966432d24b0cb79e2ebcb65280ce8248a31`  
		Last Modified: Mon, 06 Jun 2022 22:23:23 GMT  
		Size: 27.3 MB (27347519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd927167c75021e878fd8d0927d91affc71fc2a4e099b9c4fbab2d9230f68492`  
		Last Modified: Tue, 07 Jun 2022 02:28:12 GMT  
		Size: 6.8 MB (6796121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f9c7747d58c8108a20268f5d5b0603de8d390dfcb3d66f0bb462ed4757290`  
		Last Modified: Tue, 07 Jun 2022 02:28:12 GMT  
		Size: 3.6 MB (3565227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04747b6263a57bc12429b7c92af3b57c8ae582309a19f04352c61a18dfe62bfa`  
		Last Modified: Tue, 07 Jun 2022 02:28:28 GMT  
		Size: 39.7 MB (39676725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58e615e2ea48e0e32f51f5065065f925c5a3bd507f77f3710270b5fbe764c246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79971011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3768a3bc22b04004c78449beaba9de467a7649f04d8745febb85817d4978bcb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:52:00 GMT
ADD file:243d0f716fbef71d7d9cc76cf15c0b298f5b3460b6533ab2a8e88b0d618dc144 in / 
# Tue, 07 Jun 2022 05:52:01 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:42:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 28 Jul 2022 13:43:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88f853be8de2fbdcfad5b9be55e0f368887c6cad36efaf35cc75b81a8ecd9841`  
		Last Modified: Tue, 07 Jun 2022 05:56:37 GMT  
		Size: 24.7 MB (24676229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f67d1a7025edb266493591734393f4177012775b8aeba25d79ebdec1425e1b`  
		Last Modified: Thu, 28 Jul 2022 14:04:00 GMT  
		Size: 6.0 MB (5980129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d7dfebb9d6488d18196627c812d72886426c320c9793cbe601e30090396441`  
		Last Modified: Thu, 28 Jul 2022 14:03:59 GMT  
		Size: 4.9 MB (4900633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae641c620554e2616db8c77880cbc3b6b0391c65172f659563c4b2ab1345529`  
		Last Modified: Thu, 28 Jul 2022 14:04:28 GMT  
		Size: 44.4 MB (44414020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:79e271176c69a7660b26625a1c7bd384530ac8f31d3d77a6d19a699070296c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75151022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b7a3c5a62b68fe2a98e6e089fe565441eaead208f4f4f348ddcb234ca48c46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:08 GMT
ADD file:9a13d2dd4ecc4e3136c25a7b16372d77ee8ccfb9b3fcafd78af5797485ffb038 in / 
# Tue, 02 Aug 2022 01:19:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:39:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f229a80be8f0f33867b5a29c230954f11922f0e641aff2a6c16048c533bf5290`  
		Last Modified: Tue, 02 Aug 2022 01:21:12 GMT  
		Size: 25.6 MB (25575171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fa5256bba7c1c373d0a1ef1a0465e7994cf5726371518dc47bc17dde7bc45b`  
		Last Modified: Tue, 02 Aug 2022 01:51:54 GMT  
		Size: 6.6 MB (6622247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a514ca1576757eb70513da350b92d860ca64561744d13659787f0224196f53`  
		Last Modified: Tue, 02 Aug 2022 01:51:54 GMT  
		Size: 3.3 MB (3338957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0973ec85a49f90f8cd56e042492c9b81693d2b9c27b1fcb4ad9660d506a262`  
		Last Modified: Tue, 02 Aug 2022 01:52:12 GMT  
		Size: 39.6 MB (39614647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a8a9443045b57b3b2a775fb838ced9658440769f24c8be045285cbe51dc6c4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92116091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602b1719d289f9803a2586a134f720ab997692be5b85bcacf6ed4f1569bd3ddd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:47:11 GMT
ADD file:94cf6534c6b66a46a13144239fd0bba4180772804f5826d12fd030c1199457bb in / 
# Tue, 07 Jun 2022 05:47:14 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 23:25:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 23:26:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 23:28:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d9ce8aa65c6465c42b081a5642262f289b2db6cfd58b6e49f7f2c24742205c2c`  
		Last Modified: Tue, 07 Jun 2022 05:50:20 GMT  
		Size: 32.1 MB (32131305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a03c5d4a4a30095b5986889adae05bbb0933ce7e48e115e1b7fd75ae323e8e`  
		Last Modified: Tue, 26 Jul 2022 23:58:38 GMT  
		Size: 7.8 MB (7802631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe96d280d0e21317e7cdab167420493ea718b004c6e2a490a3e7e242cb0db32`  
		Last Modified: Tue, 26 Jul 2022 23:58:38 GMT  
		Size: 5.5 MB (5529202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f751ab6988cdaf74b065930f90fcb1067e074a2299e6a7164d90731e2f7af76`  
		Last Modified: Tue, 26 Jul 2022 23:59:03 GMT  
		Size: 46.7 MB (46652953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:99b522e14c8fea21237fbaf799d300678137f36813db98629cacadbce1b6f7ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77628248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbed4d2d7ebc05f14797422c8e8a98c850ed37398146ba632ee34775bc40799`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 18:21:26 GMT
ADD file:7360bdaa4ea5ec8b4eb9b93f92717ed4fb377c6910368b3f1af3f2524989f28c in / 
# Mon, 06 Jun 2022 18:21:27 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 19:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 19:46:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 06 Jun 2022 19:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1df12f21536751a4a4297772577c4c96de0f5030dfb5243599bd956eca3d066a`  
		Last Modified: Mon, 06 Jun 2022 18:45:02 GMT  
		Size: 25.4 MB (25435182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665f6f3ab1186a3216e891819468ac8dc7d533ab721c7be256ba7c56bcfc03dd`  
		Last Modified: Mon, 06 Jun 2022 20:38:03 GMT  
		Size: 6.0 MB (5960974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fcae399ce23346d8006049bedfc5c045fcd5e2575d2549db9d528ed359ac49`  
		Last Modified: Mon, 06 Jun 2022 20:37:59 GMT  
		Size: 3.8 MB (3780819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7c0ccb055a215687cbefa5c726c1fae98476e4db6af3a2b75ea8eb42916d93`  
		Last Modified: Mon, 06 Jun 2022 20:40:15 GMT  
		Size: 42.5 MB (42451273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b20a67371a372b668cb40595905f38abc2dc807723de3e9853a1a52e8efe34a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be381061213e2fc9be0539a24ab5fb7261d5032b933b7a0b8e51fc67a7c59961`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:28 GMT
ADD file:6110741104bb6cdab4d1f236e0e14d83788d0d9be2c117cc21b818cbe53bb7c1 in / 
# Tue, 02 Aug 2022 01:02:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:28:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:29:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91b26e5129898f349569cdb5e70f8a6e3046baf255fc1b62684edbcb5f7f47bf`  
		Last Modified: Tue, 02 Aug 2022 01:04:08 GMT  
		Size: 25.9 MB (25944242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afb051b7b1df235b2c41c69ce633d0f3026bc2d13a7ecb55d0cb483443d931`  
		Last Modified: Tue, 02 Aug 2022 01:40:23 GMT  
		Size: 6.5 MB (6476893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c5e4c7745db385f92256fe54757ac7d96ef0485584e1ba21d24b2b7d6ad7e1`  
		Last Modified: Tue, 02 Aug 2022 01:40:22 GMT  
		Size: 3.5 MB (3480396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5876af59b8eb33cdd8bf87b6b512f61e104fade6fdddd8532c9ab1530c05ebe1`  
		Last Modified: Tue, 02 Aug 2022 01:40:35 GMT  
		Size: 39.6 MB (39564971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
