## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:a546c957fd8988186be89c750193bb62539b4014d46fcf255b5b0624fdd87438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f50962aa19f626f477ccc1d83a5c7a2c58f82d9ed60236522a10c4283117c4c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100686090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db3508b90f202b776567efc3d8a59364ad1cf351a3a715e39aa46e5fbc8c68b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:25:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:25:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:26:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2bc9af4214222561c992590ace8ae277238c112e32760c1ff3ef6caf8ca4f6`  
		Last Modified: Thu, 16 Mar 2023 05:42:20 GMT  
		Size: 7.7 MB (7739206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155d64edd9d618f19a8fecb84dfbc4cf87eff8210625c22cc9634721fba93a7f`  
		Last Modified: Thu, 16 Mar 2023 05:42:19 GMT  
		Size: 3.6 MB (3627138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231a0ed819686e9daf3eef08ba444c6b7ebd1f65cdb1fe72aef57a0f6bb50b44`  
		Last Modified: Thu, 16 Mar 2023 05:42:37 GMT  
		Size: 60.7 MB (60741678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:58f3602ee4c39695c30963274b5faeb2d2167ace201af9f3f4c6eacbf8649880
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89850583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77759cced7d3cf207131d1c31211cac9b8d4c861cb3cedfedc5392380534046e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:48:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:48:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:49:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47332fc42b573d4baf56c0357c8403f43cd7e32995cd91e98f1b63904c165edc`  
		Last Modified: Thu, 16 Mar 2023 04:08:41 GMT  
		Size: 6.7 MB (6726111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7608366f198edf1178000bf5d347ad633c37686847555ad129799eb689113`  
		Last Modified: Thu, 16 Mar 2023 04:08:41 GMT  
		Size: 3.1 MB (3104510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53730f672819fbb90234967569a7b902545c30edae9b2a899cbd60f6d11c64d1`  
		Last Modified: Thu, 16 Mar 2023 04:09:01 GMT  
		Size: 55.4 MB (55433480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd02558f0a6dfba6c29fb4fd3b69d47d7ed610742c110ad3d48dd3665b3969c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99233268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385e737702d65ec663825da56324f18677ab4add5cb2c78ea43971cfa1d0310d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:04:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada92025b6d5b0737643d0b1828f2344b2cdb92c860a121d471b8f0c87875d0c`  
		Last Modified: Thu, 16 Mar 2023 04:22:35 GMT  
		Size: 7.6 MB (7602314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d3bbdc78821c82e7efb7e6b25412a925801281a52d89ff278c1440c1682f2`  
		Last Modified: Thu, 16 Mar 2023 04:22:35 GMT  
		Size: 3.6 MB (3617260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f381dea6869d6e20db1531b80e454b1082f1678f0397903199ce41446330364`  
		Last Modified: Thu, 16 Mar 2023 04:22:52 GMT  
		Size: 60.8 MB (60817533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:65ea078073458f501b145217e5ae0912024a6c3050c7fdfdb16c43f7167d7a5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116034160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7ad1554b25d8c56d16aeaaf445fac6e83b41fdbf9d30033f714ee0d2df88e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714fae693c74669418568b2a270066a28e7e561eae1ff8896650c09e925c0e0`  
		Last Modified: Tue, 18 Apr 2023 01:02:00 GMT  
		Size: 69.6 MB (69551759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b49083c62ebe88b5f10ca6d6083a9c3a50544dedd323efcdd669678b796dfb89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97960842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d473b3b8e44fa7c52afbd1368b9356f6d7fbfac2b9d6dffcd8d1054b1edf6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a73d2f132bb961264ac78079104aeb71d832e93e48e8bc52edc4cb58ed80e5`  
		Last Modified: Tue, 18 Apr 2023 01:13:38 GMT  
		Size: 60.0 MB (60018552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
