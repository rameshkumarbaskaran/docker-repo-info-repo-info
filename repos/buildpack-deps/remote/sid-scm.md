## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:73b24f23f41df2ca3f32c94ed0a90d1e0830916c2b950107047c4b22161f091c
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
$ docker pull buildpack-deps@sha256:113f37df301ac3654f57906a732dac2907f2f4967f7d564578a03bed515e0438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128697003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc357b4462639081858f52417d922dabcf25d6610916747fc72b03fb3da7575c`
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
# Tue, 21 Dec 2021 01:55:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2f1da4768c8ef0bf34a53ed37a7a7581bb0aa27f68e2047d84c74fbd9e6bd604`  
		Last Modified: Tue, 21 Dec 2021 02:04:12 GMT  
		Size: 56.7 MB (56718041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5043e115bbfce22f01bde7c2cb12cda2c4f1036cdb6ba07bfc5bd12ea8781562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123446253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc7ee1c5268e70c37b878519712024c4409269fe4ef908a1fc1e0a194db845b`
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
# Tue, 21 Dec 2021 03:04:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3ccf6e47632f9e757265ab81ed95477d5592cfb414aee5dd1d06090fb7af694b`  
		Last Modified: Tue, 21 Dec 2021 03:25:27 GMT  
		Size: 54.4 MB (54386233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9e370260cbdeed103fd9d61bb2f290cae8e562cf3bd5efa007824310d07f1141
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118440512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b318f69a30a8c0031ed3b508aafc3a1d3f2aaca3b5944881e52b13d8a4a92789`
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
# Tue, 21 Dec 2021 02:54:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:deb8a7423b98ff03e578c460463d8d500aa39ae23fc1979cb20cf13ddcf662ab`  
		Last Modified: Tue, 21 Dec 2021 03:18:26 GMT  
		Size: 52.3 MB (52256000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7c273dc7de4dce59b5f8ed00982cfc63f668bd2650e1547c4057332ece415f09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127474808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84209633428054b32d1092ea786c9601b1ad02e80d7a9bac0747c1f885ec50`
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
# Tue, 21 Dec 2021 02:15:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9ffa7de7b15c6883e577b019809e1343d6f6d9c4e790ce8ea84b0c42300324d0`  
		Last Modified: Tue, 21 Dec 2021 02:25:19 GMT  
		Size: 56.8 MB (56755865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ea5f96a7f8642240fe331691f522f13bab0a908479b739f6e6bb6c71e2539537
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131664208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1257c6b5f9744bbfb62d2635144198d35cef81b181fcdbf2f0f73cf3e254a1`
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
# Tue, 21 Dec 2021 02:17:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:edec29419a6219e77259f3179317cfa40969486314c93fb7616fdede0a463d5c`  
		Last Modified: Tue, 21 Dec 2021 02:29:21 GMT  
		Size: 58.1 MB (58133925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:51ff63fc21c9fbdddac8f183ccbbcbba2f11968f655c13d33a75c69eaa2fabdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126201434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b70ad729b51800c25ff7e32f374c0e57fa36092a2d9a03d2c6283f04ee341ab`
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
# Tue, 21 Dec 2021 02:59:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3e45696bac398ffc5f45aa4b095cbb3846957aa140d812fe650783333cdcc021`  
		Last Modified: Tue, 21 Dec 2021 03:14:31 GMT  
		Size: 55.6 MB (55554025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:983dc7d1c89a13e0aacaefdd1144323cdf909f56b82694eed167c128642f0627
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138794221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363125d8e48b273c25f430a2d0d7f88b1716c44bacd049e5d72a29f1bfa01908`
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
# Tue, 21 Dec 2021 03:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1096dbf3a5dbecdf522da5839970d63cb8589b951877bd58c31e92246412b7ba`  
		Last Modified: Tue, 21 Dec 2021 03:34:20 GMT  
		Size: 61.4 MB (61384627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6b91da13d7013eab079224fbd7fa095000006ed0df6803da49afa74fde9ce696
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119768333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea75dc836ca3dcd73c98a3517af8d39cdd357c584e767e7f30a3882d930c52a1`
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
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dcbe9f0dfaae59dab269d61bc7aac9b220b8a11ecf87e7d68363616bf33a5275
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126239873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc06ff58e120b7c90b2b3c3223a6dd61273bd918e5ee96c3f702159fb331957`
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
# Tue, 21 Dec 2021 02:12:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8554ce38b98712645df3c9898c381e1ac40835d50f37d436f4f4ad142ee4a654`  
		Last Modified: Tue, 21 Dec 2021 02:19:27 GMT  
		Size: 56.1 MB (56095731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
