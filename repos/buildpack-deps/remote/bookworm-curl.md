## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:ad92e74b0a112cf06f6c03bfba348f67db180a4c26ed0e44142960954f1999ff
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
$ docker pull buildpack-deps@sha256:4a8fb00b4241f71db9e0fcd6bf25605f7c4bdc229e661c5d8f0abee35d03c7a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70648936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebfa28703da32113bcd0afe313af6e1dac057326305165874bc2079b5f97405`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:17 GMT
ADD file:bc800ccc3502eee52ab13da7e930beeea45bff7ec8e6f625f2958550a0e0c4a0 in / 
# Tue, 06 Dec 2022 01:20:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:11:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3d5213c1b98149df5de6014f7a0822d3f7c1239b55b191918b5019861d2385bf`  
		Last Modified: Tue, 06 Dec 2022 01:24:15 GMT  
		Size: 50.3 MB (50260519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adf3c7a7c116d44387858d478529693ecefc787b2f5ab45aebdfe6884125ff8`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 9.0 MB (9019439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a4bc2fe30909b334399b20974788d0da585394e55d471a14a5f3e60134f81d`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 11.4 MB (11368978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:64057b9e717cec31b47e90e85afc1f35361d35b08d70e4dd218adc9c4dd7ec89
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68771095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b062e5414af9cc83c94f1cf6e98dc97f4c1e0f149c0eacde9567cae3546daf53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:28 GMT
ADD file:1a47719ac251c6eab2626d584c016fd54fb5ad1212453da6f254e2977d844ec9 in / 
# Wed, 21 Dec 2022 01:48:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:16:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5a2ba72506fbd85b58dc5575f5616efa7992eac16768aa35e10922a41b5bc83a`  
		Last Modified: Wed, 21 Dec 2022 01:52:47 GMT  
		Size: 49.3 MB (49285345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c480e4f144d3171b1600a48c85c8893cb2e7068df99ac2a593073fc603175c6`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 8.5 MB (8471399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe5572b5bd2366b9b993844292cd896c430947a32be55f045cd4a552447b46`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 11.0 MB (11014351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:30306070b3f15758265c090199657699b007c477fa888487c31907b16d3cc968
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65866881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a274fb3ca9af67d72ebf12feb05bc5e4cdd882eb4153231757cb56782399b60a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:57:40 GMT
ADD file:3a39343b0809f063616f72499663466e4a509b48e03fab9262c152a211f015f7 in / 
# Wed, 21 Dec 2022 01:57:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:25:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5d2b0b92caaf35a430a2b891b3ae1c59a6cf60477263bd8e7a30cda427435d63`  
		Last Modified: Wed, 21 Dec 2022 02:03:55 GMT  
		Size: 47.1 MB (47101260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a36589bec34c9187227f581132ae596646abfc864ef9c4f049dcc7cb80d9e3`  
		Last Modified: Wed, 21 Dec 2022 02:36:46 GMT  
		Size: 8.1 MB (8119430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa4da363e919b9e1ffa0593e59ab1b23caa6d60c84b20ebfea4db0863532e5c`  
		Last Modified: Wed, 21 Dec 2022 02:36:47 GMT  
		Size: 10.6 MB (10646191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:378382ddec1488681bd1161587e8e5a06aa4348915e57c78cbd62909f1f2bf42
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70548006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd876e5df9a18a4d5c8245d88fdfb346ea31f674627ced5ee7615120b532a102`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:25 GMT
ADD file:b83d427ad5bc07aecb363a59c19809d66f1425c1d8df7a4d66eb56624cf5fcf3 in / 
# Wed, 21 Dec 2022 01:39:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be520eae96ff7c486efeba591ba872089e3b618ce226d23bf2b72f07277fb6fc`  
		Last Modified: Wed, 21 Dec 2022 01:42:15 GMT  
		Size: 50.4 MB (50372842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd22e8d17dba55cc72a876a3a9244c7b617edbf94a17fdaad2f9d803c02d5f`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 8.8 MB (8849270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7950c3893d7d3fd9cc5fb052ba3abdcdc532147811125fdba6efec5d9b4efee5`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 11.3 MB (11325894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8d5fa6d85d1f5df8f8c7d8253ed9c8296d352e48e9d780cec70d454fc70f12df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72058952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b86fdcd6d324de17f304a77d442a0882677f97eefad5d51a8affd980858972`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:38:43 GMT
ADD file:6064ead20e3d5415784fcb74157c3ba1b90982f542deb132e9dabb2a1712e396 in / 
# Tue, 06 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:05:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:05:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45070d389a5ecd4dae6cdcb3e06567c8481416cfb2efb085e318fb5e2d11393b`  
		Last Modified: Tue, 06 Dec 2022 01:44:36 GMT  
		Size: 51.3 MB (51301574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe8313be6a60f2abeebcfad5a2e4539e7d4b28618e0b019908926dd39c9c1bd`  
		Last Modified: Tue, 06 Dec 2022 02:14:11 GMT  
		Size: 9.2 MB (9196657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa4a90125b538cbb0d87c8c0d37737cdc01ed561a27c8ecfae4cc4f708aecc3`  
		Last Modified: Tue, 06 Dec 2022 02:14:11 GMT  
		Size: 11.6 MB (11560721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:48a85c6026635767f34eabfef5e647c785a124e44552629cad4ad5867833f94f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69762043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1069f62c88f828192bbed9ad7347dd9febc10c0216b7f9974bf211ce1f21fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:53:35 GMT
ADD file:5f771b53cd80db61f6fcf0df30ca6b99cd2c768f57ab1ffdf53d1f646b7db7c2 in / 
# Tue, 06 Dec 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:06:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a9cc4004cb6d73c258a4d864dabb35e2beb3272eaf0de591430b0bb1af15141c`  
		Last Modified: Tue, 06 Dec 2022 02:01:46 GMT  
		Size: 50.3 MB (50259491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb8986f763b3dee4c5b32d9c82a018159c1bc6452e370fe08635660e89d7fe`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 8.4 MB (8384079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60f3afb7af77661e81375d03b106172646d324a7f36dcc156ffe006dd22158`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 11.1 MB (11118473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2069610b204e2b3407e66e9fe4c715ae4c3c85b940752e076ac3f3887c8762a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76046478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513f00fe77dc724e1e75ee76cc576d60d3432b2e62be90e2b43eb9b89025075`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:16:54 GMT
ADD file:394004d3191138471ba2dd50891718f9142a137ec9018f4f69a653139a98abf1 in / 
# Tue, 06 Dec 2022 01:16:57 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:35:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c1206773e59171c1200c3692244202cc0da97f8fc41cb86ed64f742f1e75b47f`  
		Last Modified: Tue, 06 Dec 2022 01:22:51 GMT  
		Size: 54.3 MB (54319290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2bf8fe0b01dd711eba4372279b1ec1baca4dda44423540050ddc904916d0bf`  
		Last Modified: Tue, 06 Dec 2022 06:48:23 GMT  
		Size: 9.6 MB (9598813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594f52d0cb31836574048a516ce0e264a5125592606d1b50484ce8dc7c4f0b92`  
		Last Modified: Tue, 06 Dec 2022 06:48:23 GMT  
		Size: 12.1 MB (12128375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:036132d70a14cbfa3a43131ccfc091d033c3f8cb8988e2773a64162221998275
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68544375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290f812fc20133b9d55535b8cd6775dcd6a1dfb5213570652e779f20bea521e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:45 GMT
ADD file:45186e2067a128e8dbf3558a97cd5853548faaf7c2bb93ef1544ed66907fcf19 in / 
# Tue, 06 Dec 2022 01:41:55 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:effa21bde36181862f20d53853fc03e36421f6a13d6aad41051d593fe9c7c097`  
		Last Modified: Tue, 06 Dec 2022 01:47:58 GMT  
		Size: 48.7 MB (48664905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f5dcd56007991a3866c8b0bf2ee7220f18a57fb48ff74112e6c810f63c8b96`  
		Last Modified: Tue, 06 Dec 2022 02:18:52 GMT  
		Size: 8.7 MB (8652754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1216521a137ae490612192a50d936077fcb94da6292a8ef16485599b92a5ace`  
		Last Modified: Tue, 06 Dec 2022 02:18:51 GMT  
		Size: 11.2 MB (11226716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
