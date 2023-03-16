## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:4496242c34cfa7b0d19f49404dd3439cb860bfc260638be772a0d8d29310e5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dfca8dc06d26d3a6045ceef176d672df2185198782833ce82c81f3417487b7e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82293840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db010a0e4873cf66ebbbaeb58004ef354ea6507c99ebed518c311dd06e6fe4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:14 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:16 GMT
ADD file:a99f804e480d9a1b56aff6406b4da5a3dea89f11f968e5e02cd4ba5a25e9a7bc in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:37:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 03:38:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6347900c239eb6451b578d272779198ff2efe221eb716c1ee35bb33b3d36c805`  
		Last Modified: Thu, 02 Mar 2023 03:45:59 GMT  
		Size: 27.5 MB (27450641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635fc9b499f00984f063653ce41c5bcd7a2101d4709bde16211c9cd61cf53c97`  
		Last Modified: Thu, 02 Mar 2023 03:45:56 GMT  
		Size: 6.6 MB (6637316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583126b5de1692321379f3ac3c479e60776c2630177157537ce16c3b5310534c`  
		Last Modified: Thu, 02 Mar 2023 03:45:56 GMT  
		Size: 3.7 MB (3690222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4e53abb79424a77d128c854eb7fbd2dc2baf538b9618ecdc1377d5c513a4d`  
		Last Modified: Thu, 02 Mar 2023 03:46:14 GMT  
		Size: 44.5 MB (44515661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:13ccc3def0daf769539fd0ca304f2a28da88d5bb794c46c1f93916f458251517
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84502342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a304d21e8dd95ea8eeb55ef412cc1ac9bbd4acf5075c01142941f14b6f9005ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:43 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:44 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:53 GMT
ADD file:e4ec0e899927e1fe0388f3524f3382183df8c74bcf9de0e35e1c8120acbc2b7a in / 
# Wed, 01 Mar 2023 05:41:53 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 11:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 11:48:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 11:49:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3149fccce04237916ad21629e6497df2edac53a12b13cf63470e4ee5833f8e4`  
		Last Modified: Thu, 02 Mar 2023 11:58:22 GMT  
		Size: 26.2 MB (26236811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1c91da9e0e927655ec912d3e65425143bf9d0dc2bde931112305247aa3dca7`  
		Last Modified: Thu, 02 Mar 2023 11:58:18 GMT  
		Size: 5.8 MB (5809168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ee07824f253241f1cd1a7d308e85f8d6bfdb3649f0d1db1d5c49d1b1ff337a`  
		Last Modified: Thu, 02 Mar 2023 11:58:18 GMT  
		Size: 3.9 MB (3852238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307ab9ceb5b6a487ea64bb9ab76e4c75483c4dd388afefcc036953ad0170c750`  
		Last Modified: Thu, 02 Mar 2023 11:58:40 GMT  
		Size: 48.6 MB (48604125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4d2316040e83fb85fcf5553a00d9884e58bc4ae0ac45f809513198b31164f7a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81368243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78899799edcb9bb2076bbcfe6bcfb75f1dffa05836b5c21617593bc97cd03734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:30:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 02:31:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6700b5ef6bf750ef532062fc9dec24b7d9247840b877f26af1f339df77db5ba1`  
		Last Modified: Thu, 02 Mar 2023 02:39:03 GMT  
		Size: 26.9 MB (26899339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01eb5985b1759d7a00fafb6eaa0426c9ba33b24bab18656ae5ed19b74869bd3`  
		Last Modified: Thu, 02 Mar 2023 02:39:02 GMT  
		Size: 6.5 MB (6468687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5136aa3449032f883f29b10908230ca4a5c79c1a4fcf12f1c28fa763b07ac0db`  
		Last Modified: Thu, 02 Mar 2023 02:39:01 GMT  
		Size: 3.6 MB (3649336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99899628512ddfc061595eb4f812d31ea2842eb378a4f491eb3ab8c133270a51`  
		Last Modified: Thu, 02 Mar 2023 02:39:17 GMT  
		Size: 44.4 MB (44350881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:39d5d1468937ce1cd50fdd52cb7dfc5d713f2a7494ac3925626f12ee6e417278
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fbab15a93c2f95048c838e9d8a6e32252fb4b63ec05dd2b4fec7ba3acaf270`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:58 GMT
ADD file:dd48763269678622cf7a1219a8b87a1222a24048b5cc1ab133a42cbb854c7f78 in / 
# Wed, 01 Mar 2023 05:00:58 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:45:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 03:47:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:434ae6294eb01eccffad6e8e39b3f373d83e33cfedaa3f3cb70962a1122776f0`  
		Last Modified: Thu, 02 Mar 2023 04:01:02 GMT  
		Size: 31.9 MB (31897489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316ed6bd69a08f1739325fc66aebcc6c5bf34087b52b0f3a2e4bfca0c109e76d`  
		Last Modified: Thu, 02 Mar 2023 04:00:56 GMT  
		Size: 7.6 MB (7606587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba7fe918b6d86615ad6aaad9cb8d4e29030952575a61624dbb8f5e15f5ca8f9`  
		Last Modified: Thu, 02 Mar 2023 04:00:55 GMT  
		Size: 4.4 MB (4409088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0e010afca98d127a9b0d8607ac999fc79b19e8d612c6fc6e3a9e1ee1a1de76`  
		Last Modified: Thu, 02 Mar 2023 04:01:28 GMT  
		Size: 49.3 MB (49321485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:be8e1571ea2945b768f155c85a9fc4d617a62103e27b12291a1b9e88c5ae2f53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80254144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad371214c349f4a458439e817f999971228fed0bcf6aceaccbb08508cf9c8a0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:47:18 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:47:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:47:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:47:20 GMT
ADD file:1ed4a1aa279c8c4fd49f73ed214f53835caecef222778b80716ba71fe60cc7f0 in / 
# Tue, 14 Mar 2023 17:47:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:56:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:413472b726c3207e3bafacfb65a3db7c0c8692445502e7d2ad70b1585e534841`  
		Last Modified: Thu, 16 Mar 2023 02:04:26 GMT  
		Size: 26.2 MB (26162786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef961f5d29313e42026cc5111865e26af7782293f64f5eca11172750d63f804`  
		Last Modified: Thu, 16 Mar 2023 02:04:24 GMT  
		Size: 6.3 MB (6335431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b09797bd3d78e6694a4d023216c32e3665a913d5dcd639c47a00674aa9bd5f`  
		Last Modified: Thu, 16 Mar 2023 02:04:24 GMT  
		Size: 3.7 MB (3674242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ac168459f3e70bf00dbc80bd6a3cca0005c0e36d3ecf7fd0ae2395921677c5`  
		Last Modified: Thu, 16 Mar 2023 02:04:40 GMT  
		Size: 44.1 MB (44081685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
