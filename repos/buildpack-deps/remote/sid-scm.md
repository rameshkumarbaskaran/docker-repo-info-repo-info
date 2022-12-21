## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:ae83a11b4222aedb38e21b3bbffa2b641b40c917b13af02bcdff1db07587b8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:abb04a9b0d969fd305699d86e8d5d28ac53f38e4178780b746d44ec539fa5831
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131669292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c94e18229627b6510f81c9c87c0ead91934ac4b161ceaf1dec48759cc994c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:52 GMT
ADD file:643fde45a6d11f36b1178a022667e74288e58a263ac7999c7cb023cb3fcde3a8 in / 
# Tue, 06 Dec 2022 01:21:53 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:17:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8db6e5cd5802a750fd04af4eb64a857f779b9c2333d2d830a50d7b2983365c1`  
		Last Modified: Tue, 06 Dec 2022 01:26:42 GMT  
		Size: 50.3 MB (50309617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b904b10ee4925c81495d781c9278243be45e6e2feb4350d4e8780c3c15c9d65e`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 9.0 MB (9019750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826135e5b952effdf73fc4ca5766716e2efde4728890f709a8e0629212bfb80f`  
		Last Modified: Tue, 06 Dec 2022 02:23:48 GMT  
		Size: 11.4 MB (11369325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1a31718aa1aa53871a059e3a80e9c5bd0d4a6f8fd55a8cc63db471e6014006`  
		Last Modified: Tue, 06 Dec 2022 02:24:05 GMT  
		Size: 61.0 MB (60970600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f98ea91970e25833ccdcbcd4f9ca3efec9b9c340eec97d85f1b2011170e8dd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127127389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823ada119b52e40faf340e6eff77a3c79b2f0f30c9dc3b6bd6dbb4a379a68083`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:19 GMT
ADD file:7e649d148f5ac98acdfce2b45b373b5b22a9792e3d365d3f1dcb2414a59f4149 in / 
# Wed, 21 Dec 2022 01:49:20 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:22:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:22:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:22:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3175fea42c68213e6e72826c3ee7daa4a58070ce07ae526e91c30a8743d89be1`  
		Last Modified: Wed, 21 Dec 2022 01:54:28 GMT  
		Size: 49.3 MB (49270781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2f8a381ecb39f18e385e77a8e8d6e9d27b631c659084d0d9a3a82c5e9f9b47`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 8.5 MB (8463955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681a42b466ccec4b7ac8c821ac8ac7d1787f7968ea77629bcfd8efa108d32f4a`  
		Last Modified: Wed, 21 Dec 2022 02:27:59 GMT  
		Size: 11.0 MB (11014376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf14e116100aa5dc86d38341ffec41bc259ac037aa38c189caa7b1d9f1d7f56`  
		Last Modified: Wed, 21 Dec 2022 02:28:21 GMT  
		Size: 58.4 MB (58378277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ac1fc2aad3a34c055d0fdba3cabeeb60bb1de6f348aa2fb112746ef399009332
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121888730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbaa85a28d32b846d28be7f671d920fff2780789e7c8c5daecdd61d56318c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:31 GMT
ADD file:9f6e7ad60906ff390d6369133d129df5057cc1505edafd2cccc2eefa5265ddaf in / 
# Wed, 21 Dec 2022 01:59:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:31:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:31:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d12d04403dcef32bd0b6201954d02c0de421dabf04dd54d568898f376cb96c5`  
		Last Modified: Wed, 21 Dec 2022 02:07:07 GMT  
		Size: 47.1 MB (47080683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36680a9d2eba076180efb89a2b7a21233fc4e0a38e383b2c389f543e56a48be`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 8.1 MB (8110360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edac00689713d5d2b7fdcc4f1c017ec260832d0c2a65021c7f013a4a71c9bdf0`  
		Last Modified: Wed, 21 Dec 2022 02:40:30 GMT  
		Size: 10.6 MB (10649074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb2e96f612174a7d5711371774c88238e9809c0d631f6a0e50ee1591e53bfc`  
		Last Modified: Wed, 21 Dec 2022 02:40:51 GMT  
		Size: 56.0 MB (56048613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08d2f7a616113680eaf26871efece80e9fad1ca3afa715a34f127fa95202b09a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131173276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f06580932d0b393e404f8dd737ab3a571d0feec26636717b103654b98bd293`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:22 GMT
ADD file:afdb0d23dc73b5f1a887a2dfc3fb8fc2ebf210e9ac6b5d6748cd89c77d9e436c in / 
# Wed, 21 Dec 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:09:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:09:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:951a6c4c03238810abf592f0f3beb641ea6b4153bfa55acf62944018b9ed669b`  
		Last Modified: Wed, 21 Dec 2022 01:44:40 GMT  
		Size: 50.3 MB (50335976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdda1c5e6e87491ced136c13ab5b4f5638649dbeff005a13d621df9a094822a1`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 8.8 MB (8843497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae130f92dbc53edf856d24c52cbf32f0410d34ccacd94bac928422ef4f4fc7`  
		Last Modified: Wed, 21 Dec 2022 02:14:29 GMT  
		Size: 11.3 MB (11328912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c026988df51d7264167f40103dd5c01db4eb446f90f5f6787ce90289773298`  
		Last Modified: Wed, 21 Dec 2022 02:14:47 GMT  
		Size: 60.7 MB (60664891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:158f00acd554547447e20895448ff9653122e43067e5269bac4741eba913fd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134967863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645e33887841a2fcc3124c0dbba86cf4aaaee04d3d81cc9e938f84abfc4aa09e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:02 GMT
ADD file:0909d182d8916b1b37783d0c3582c9d3f3edddf6cd27e90100343ed0462c9c75 in / 
# Tue, 06 Dec 2022 01:41:03 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:10:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:11:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cd5a2a4c5902ff854cd1178702a69271f9bf768ae5b99124c16b51e5c2d42a1`  
		Last Modified: Tue, 06 Dec 2022 01:47:24 GMT  
		Size: 51.4 MB (51358972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5c5bef3805a0d8c076d12c22f99b0c27a09807eb93eeb57ae35352e352cd30`  
		Last Modified: Tue, 06 Dec 2022 02:17:38 GMT  
		Size: 9.2 MB (9196899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbaac64d951183e4d1471ee19eeb170556b928f547c45a65c32e7c20445e6bc`  
		Last Modified: Tue, 06 Dec 2022 02:17:38 GMT  
		Size: 11.6 MB (11560888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd513eeb45b150b04634e02e8766f804f8249d25bdf16f0e34bb419a67b46d3a`  
		Last Modified: Tue, 06 Dec 2022 02:17:57 GMT  
		Size: 62.9 MB (62851104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:999a1a8a7983de5343333637880de9f1aed2dc96f530547624a68eec3b94fa0d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131896713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1c98e2ed4dddf1500242d88ae48d3fa9bb7ed8b69deec8b9e69ccfc99f4b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:56:07 GMT
ADD file:f0c5ebbf2aa59cd4e0996c808ed4d378c47b86ca4c00f63fa5de02b4cb838334 in / 
# Tue, 06 Dec 2022 01:56:12 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:25:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfb5e33f7f324b83c5e49e84922c9f448eace01382dd0e6ac683debf1a61eb39`  
		Last Modified: Tue, 06 Dec 2022 02:04:23 GMT  
		Size: 50.3 MB (50319836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b834f7ef2a923258cac3647eea1dc30607526608cb7736365eb762f58302d`  
		Last Modified: Tue, 06 Dec 2022 17:39:24 GMT  
		Size: 8.4 MB (8384243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bab24553411999fc0ee1271fd159e73a742187f55b55da1666e8215102677`  
		Last Modified: Tue, 06 Dec 2022 17:39:25 GMT  
		Size: 11.1 MB (11118815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e22a8513c4ccf09821ec9d4887f64f4be99e05b4a5b5385317c5fa9ffba1e`  
		Last Modified: Tue, 06 Dec 2022 17:40:17 GMT  
		Size: 62.1 MB (62073819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c41349b2e21996400d1b6238de44e9e0a4b3922352d4c396d7e6c17cbdf547b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142544829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80780f7d8b7cbe651690e7babccd0f0ede588910a814aa0aa3c69d87a1c9e43e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:18:26 GMT
ADD file:bdb06f846e6364870996f9ac20fb236d99a0ac4e61f11a82dda8599bbd6ea354 in / 
# Tue, 06 Dec 2022 01:18:29 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:42:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 06:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e30927c2af9840769d712ec0a0e33b7ccaba3ec9a715660e8c1b04953084dec`  
		Last Modified: Tue, 06 Dec 2022 01:24:47 GMT  
		Size: 54.4 MB (54361158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78655a02977225694ec4b2ed16679949be76009f0b14a3f968d3cdb59c8b7f5`  
		Last Modified: Tue, 06 Dec 2022 06:51:46 GMT  
		Size: 9.6 MB (9599186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7619effb72c38f135dd9a28562bd32fe00ff1e2195159f614d39b386aefaff`  
		Last Modified: Tue, 06 Dec 2022 06:51:46 GMT  
		Size: 12.1 MB (12128850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7e852d58e4283ee04c5a1f76c638b6ab081852cd1e2637b9af1d5822cc7267`  
		Last Modified: Tue, 06 Dec 2022 06:52:14 GMT  
		Size: 66.5 MB (66455635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:80fe5d929462fbcb8fb502564ba1c94f3a1fb305aff0e201341b695be50f3fd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122015209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3095c5914c0792da561d083de7026417fc5bec6e01a866d86b2f8f8d796eac27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:08b39d8f5a76ac300c62fc1f9d124bedbde4dbeec05ae29c8c735c37efe48ab6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125601702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc772f5fc3dfb795231ec60b89702c02f79a3d52061d99f8b99bb057500d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:43:23 GMT
ADD file:9c101517ec1598b49e898a5a60ee79d12ae039f3da76a37f4b9ecc5211ece070 in / 
# Tue, 06 Dec 2022 01:43:30 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:12:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:377056d01f15b8c008b4b2d5e74aef86cd1b3c25771df79e7a3d4592cbbee6d3`  
		Last Modified: Tue, 06 Dec 2022 01:49:02 GMT  
		Size: 48.7 MB (48699631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ad70c75e8b0ca75e558f3a54c3713a77da7920e04007e9375d34fc22d8ab7`  
		Last Modified: Tue, 06 Dec 2022 02:20:36 GMT  
		Size: 8.7 MB (8653107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ee9f87d81b16e0ab87064ce67465efa2eb9ba18cfc708c866166dc66456f13`  
		Last Modified: Tue, 06 Dec 2022 02:20:36 GMT  
		Size: 11.2 MB (11226859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f13fee19d213256041cffb5312439af3f291eecb89cb788bd2a15a73301e62`  
		Last Modified: Tue, 06 Dec 2022 02:20:50 GMT  
		Size: 57.0 MB (57022105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
