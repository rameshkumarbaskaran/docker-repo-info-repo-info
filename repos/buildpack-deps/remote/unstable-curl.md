## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:098f5177cbb24bab17d6970deff56ad62dcf656c9a4325cb7426fba400479736
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e8c5489263d3a0c33d1ccf0d1aa6cd69849aa552f8b48998b3444623981f2bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71978962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337c9767010b746d2cd95bdd0271a57eda89683bdd979326eadb8efeb5f016a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:53 GMT
ADD file:ce4b0836a3fcb4df3c14bacf996ad27dde10d17f63fbf745c09d6ae62c3e2cc8 in / 
# Tue, 21 Dec 2021 01:23:54 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:54:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:55:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4c476fbbe1d7eecc32473e300b1659f1eaf7c11eff20d52cd6f7471c94062564`  
		Last Modified: Tue, 21 Dec 2021 01:30:07 GMT  
		Size: 55.8 MB (55798023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c6bd99048b6b72b33b515cda942b7e40ca1d3de2b2f9cdd7bcb90dbb74274c`  
		Last Modified: Tue, 21 Dec 2021 02:03:54 GMT  
		Size: 5.3 MB (5276774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492abb693e033360d88b0b5fc39af18ee3a635345217fb4fa41328e278d7136b`  
		Last Modified: Tue, 21 Dec 2021 02:03:54 GMT  
		Size: 10.9 MB (10904165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:73316152eda6c580b60bf8eb39ed3f90ad39b6b9c7db0489e0132e29e6327f87
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69060020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9431be8e15f22f684715075cc33a56cf502b1929d95d9cfec37e46397f3ea7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:53:50 GMT
ADD file:61604460e02950a274e51fc98393073e2b68e279308b9696e87d53530bf47fc4 in / 
# Tue, 21 Dec 2021 01:53:51 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:03:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2252da0fe003db28a23847a348e614635e01bdee48388ba4a2e8f08591bb48dc`  
		Last Modified: Tue, 21 Dec 2021 02:10:36 GMT  
		Size: 53.3 MB (53269288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb0227efa1a180434991f165be712afbd262dce6a1fb96d1e06a75dd6c15510`  
		Last Modified: Tue, 21 Dec 2021 03:24:34 GMT  
		Size: 5.2 MB (5180246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1befa24c2479fa4c965693e683ea2899180a18f0f5e15a301ad8367add88cc`  
		Last Modified: Tue, 21 Dec 2021 03:24:36 GMT  
		Size: 10.6 MB (10610486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3b24ee520acc8b008c33316e7b456f65942f3a71e8a276971473531283336039
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66184512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b247547a4244d82f80473ce060588cd966d88a31a7650729c3e66dc683b5c3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:03:18 GMT
ADD file:0d5a8f9dfe2d9c5be9a0c7bc6937d1eea64c660ed161e798c852f8e3998ee095 in / 
# Tue, 21 Dec 2021 02:03:19 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:54:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8e7bae00ea7d8195a01bb9d7101851880c4ca29ce9c6a4d32acacd59ce6a3436`  
		Last Modified: Tue, 21 Dec 2021 02:19:52 GMT  
		Size: 50.9 MB (50894650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc192de0e363b378b3d0c50ee0848801b2cc09a505a5242566d80b83658e843`  
		Last Modified: Tue, 21 Dec 2021 03:17:32 GMT  
		Size: 5.0 MB (5037229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3403b6d74fff353f4564db0a15852a0d94b1910fe6e3687121c5fa14ec5046d9`  
		Last Modified: Tue, 21 Dec 2021 03:17:34 GMT  
		Size: 10.3 MB (10252633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6031a1d48868123430f79c3b69e7fda462caac3a9389dfff4fca4f52e5b71f7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70718943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f15b4dc686153d9a24fab3d2557710fb2428d1c15c56136539f3c38e1b56fa2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:45 GMT
ADD file:7c4ba9d9936c0139eeef9f235c0d6840aa3c32d40904663e82e285a1b34d3a75 in / 
# Tue, 21 Dec 2021 01:43:46 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:15:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ff79c5138bd3b6ae9212e3b674731e907981317ed2018a35ca98f456034d18dd`  
		Last Modified: Tue, 21 Dec 2021 01:51:23 GMT  
		Size: 54.8 MB (54780864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04ea6899cdef9e4cb3add824a5c066cfe56407ffa977a94114981f8c9e02493`  
		Last Modified: Tue, 21 Dec 2021 02:24:57 GMT  
		Size: 5.3 MB (5263545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6eba4116602817637a346f0e2c8ed4adf77ba0f6d395eb6b49df6d42761b6`  
		Last Modified: Tue, 21 Dec 2021 02:24:58 GMT  
		Size: 10.7 MB (10674534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c7ec0bd38ff25ecfe5683611d8c90adda8b08331bdf343e31a697e7254228543
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73530283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523f783917916abbc3c08c9911b21aeb61dc7282e093bdb81fb6bd2184291930`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:07 GMT
ADD file:7c506c9d86a63bd33b2bd42ba9e380551bac76c3ef7352900f2acd644f4c8540 in / 
# Tue, 21 Dec 2021 01:42:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:17:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:17:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4134c3f595c8eb15f3af8157a618c36c51d0cf4948eb0bc00ce1697bab8e3d81`  
		Last Modified: Tue, 21 Dec 2021 01:51:54 GMT  
		Size: 56.9 MB (56851682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39f58d3b3754f23bbc0ceaf7adab7ffcc255c02bf6a043aff6842dd0cd45d`  
		Last Modified: Tue, 21 Dec 2021 02:28:54 GMT  
		Size: 5.4 MB (5408518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769abd0d85d00c570f55ee96473cec596d53c5a8292473578a15779b5e36e82`  
		Last Modified: Tue, 21 Dec 2021 02:28:54 GMT  
		Size: 11.3 MB (11270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:30f1a99fce643fdb0f9add754f54c64b5be632537f9d3aed514f3aa5c3418b61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70647409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22fc6527a3097253fe23ae6680eef8e56c4277ca301d8657836d753f1e0dae3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:11:24 GMT
ADD file:03fe06379d2aa624e1b4f2fa09346703a6e044943801a3b71ad48db009afda1b in / 
# Tue, 21 Dec 2021 02:11:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:58:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:58:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1b2781e827d3c7d5377a11eaa940ec91a05b3c9be49542abedda2252f7b4fd82`  
		Last Modified: Tue, 21 Dec 2021 02:21:58 GMT  
		Size: 54.5 MB (54503889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831b577e1c4668fee3d0cfe74f3d2215a337eda6285705829c5761ac52d24433`  
		Last Modified: Tue, 21 Dec 2021 03:13:30 GMT  
		Size: 5.2 MB (5235777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc2b6c4969cde98966d9fba39c75427177d2b73763f69cd64e55f0b27cacd`  
		Last Modified: Tue, 21 Dec 2021 03:13:32 GMT  
		Size: 10.9 MB (10907743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:610577639497c9fb19ac42ef666e0930d7c5a4bbe07cf4f71536a83e82ad3582
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77409594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3d8c55e6acbd63fb1c4a4c8b490c442d685b9d433985a1f77b29649c20f952`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:22:14 GMT
ADD file:641bd15b93416ef98057364d15a9dc024ad99715a857b95b132e59fa84794dc9 in / 
# Tue, 21 Dec 2021 02:22:20 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:19:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1afc4e26929331434b14e0ce909f34a23e7896e101e78bc5d9426f4bde69d912`  
		Last Modified: Tue, 21 Dec 2021 02:31:35 GMT  
		Size: 60.2 MB (60199744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9340a0af36f9cb5acf1211719a4c267941994b285c90c83d471fa003822f9809`  
		Last Modified: Tue, 21 Dec 2021 03:33:55 GMT  
		Size: 5.5 MB (5538004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3d148fb84a5de0565268fea6e6c976afdc2985b95421dd2e6b55a8579625c2`  
		Last Modified: Tue, 21 Dec 2021 03:33:56 GMT  
		Size: 11.7 MB (11671846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8db4f32e3f2a1573529ece628ecbfb7945ca0f7de288f2c116627b9b7b90b19b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66951327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6297cf5e309e6a03c3b3da24395fb5ba06e91d0c9ad60d5c3f91e3f72694bb2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:235a0b08c7d7a18538bca35809aed769fcfc902e8453a5e9d5ab3376a8f1fa7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f4287ebad93a64b1bd72a9c20e0a98b3aa40aa5b57e28c386f8516bc8b948a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:37 GMT
ADD file:fef3d16fc616585749eed591688807817c9f37f8c4f5b1f6fa331e8abb0b60b4 in / 
# Tue, 21 Dec 2021 01:43:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f8ce27066e069d94a5210461101ff67f39042687acc056c6b8f43da616f6b2b6`  
		Last Modified: Tue, 21 Dec 2021 01:49:35 GMT  
		Size: 54.1 MB (54090241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430eb3656cbd2e26f5882863248d1d470bb0f7b5019c000a75107367ebed5950`  
		Last Modified: Tue, 21 Dec 2021 02:19:12 GMT  
		Size: 5.3 MB (5256801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf00a1bce82700c975dc02484e483d113ef14013f902525638bf031c142cae0f`  
		Last Modified: Tue, 21 Dec 2021 02:19:12 GMT  
		Size: 10.8 MB (10797100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
