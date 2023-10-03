## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:1d707cf477906daf40ccd71f65360370d20e4af04ef0218f7efdad6226945aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7154ee606209e01dfbdb5a98d17f4e66e941f7c1c80af9ba1f3c13303f684b38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86726599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d00e70f23db7ea7bb66c70316bc7fdc44a79fb1fd30b985055907d46d8dd27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:03:43 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:03:43 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:03:45 GMT
ADD file:5fb49f260a0c3bf404c0fe31d8f0f812e9c143bd48223c4f15a85168758eb880 in / 
# Tue, 26 Sep 2023 05:03:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:03:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70c34fc37a9391a001a8d99c74b27823143398763bcd623c3402a790006947ea`  
		Last Modified: Tue, 03 Oct 2023 05:09:43 GMT  
		Size: 28.1 MB (28079281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13daebad235cc5fc75272df7a4cd22cd9e14040be8b10d9ec3764328c7be1ab`  
		Last Modified: Tue, 03 Oct 2023 05:09:41 GMT  
		Size: 13.9 MB (13886180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5024b0813f45b8c3c3d60316917bb453d13c81a8bab8316b17b30ac61156c6`  
		Last Modified: Tue, 03 Oct 2023 05:09:58 GMT  
		Size: 44.8 MB (44761138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e198556ecbcc37ab2297352a3ff1845d949b22d85928d97229b1e457431319a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87711294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a6f4028f29d6923b5eb801f6947578178f8c808b23aa54095ed940196f8a28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:05:03 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:05:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:05:04 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:05:08 GMT
ADD file:512405a66f1049a7237c67d9d5776db7f41d5991eceec535260f4d3b7f19e65d in / 
# Tue, 26 Sep 2023 05:05:09 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:11:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70fb529e8caade31afb15a43cbaa98da4446d46bd64b25df10259be9a57f0577`  
		Last Modified: Tue, 03 Oct 2023 06:17:59 GMT  
		Size: 26.1 MB (26055984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7003bc3702b787e6176ad194751c3ba0ff76742ea89883d5b9e9bf4a15d93fb`  
		Last Modified: Tue, 03 Oct 2023 06:17:56 GMT  
		Size: 12.7 MB (12713461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe360aefbe92efc04c5f077bc27baf1ae132ca6e543274ac4e2180efca7507c`  
		Last Modified: Tue, 03 Oct 2023 06:18:16 GMT  
		Size: 48.9 MB (48941849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b90f855ca6f36a58ffa93d51518b716154ce46f2501c052255a4ca69820f5f40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85341235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1353821bcafbdc837c170ac7e68154a2784c2c9be1397d618829b032d0afd42a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 05:06:27 GMT
ARG RELEASE
# Tue, 26 Sep 2023 05:06:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 05:06:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 05:06:30 GMT
ADD file:0dbbd4de9483bc32897d525742b94aa13ebd3a6aac7f1844d94d7f4536b2bfb8 in / 
# Tue, 26 Sep 2023 05:06:30 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:18:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4259d3adacfee572bed7acadc8e4af2cf679658d229fc94eb25abeb6d662693a`  
		Last Modified: Tue, 03 Oct 2023 06:23:31 GMT  
		Size: 27.3 MB (27315811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e515aa13e7ac1bba03883084849baef28268d175299a636c354b0e7558af88`  
		Last Modified: Tue, 03 Oct 2023 06:23:28 GMT  
		Size: 13.4 MB (13394041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a515dbb7fdd56d447a83b9c10d1e2ec2fb52e85daf470e09424283d14b5908`  
		Last Modified: Tue, 03 Oct 2023 06:23:44 GMT  
		Size: 44.6 MB (44631383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:977c79d6b8f01f194b957f7275c4f50d1d671a66c30b44e19a8143013fbf1f94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97862194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff61b5ba517d57e7d5be3582786fc0eab77fff67a3c96b95be77cdead8c4da41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Sep 2023 04:43:47 GMT
ARG RELEASE
# Tue, 12 Sep 2023 04:43:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Sep 2023 04:43:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Sep 2023 04:43:47 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 12 Sep 2023 04:43:50 GMT
ADD file:56d58cbb4273b81f0c1a0b6eaede82f6a7e5d79c78d54525361f0537566dc9ec in / 
# Tue, 12 Sep 2023 04:43:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd229c9aa7cae185d030f835d891646d81b863cdb9cb773e41f12ee940228d28`  
		Last Modified: Sat, 16 Sep 2023 02:50:16 GMT  
		Size: 32.4 MB (32367087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec9bbd29feb8adb47adfbfa6309c9d863f2e8ec5f80cf30563f27da97167973`  
		Last Modified: Sat, 16 Sep 2023 02:50:12 GMT  
		Size: 15.9 MB (15938863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6f18bc37fc98bef3457686b1b305b6bc6178654b8998f68ee0fa0dcafcf065`  
		Last Modified: Sat, 16 Sep 2023 02:50:39 GMT  
		Size: 49.6 MB (49556244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0455529e5225c85cd91293b3e29caf5def9ac392c642de5efd807518abdda497
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86723954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d4c8d1fd98e9d1a0e24c2af3a3dc2a7cd9cd32a8535ade59e4011c131a0232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Sep 2023 04:45:06 GMT
ARG RELEASE
# Tue, 12 Sep 2023 04:45:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Sep 2023 04:45:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Sep 2023 04:45:06 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 12 Sep 2023 04:45:08 GMT
ADD file:6724cd2c23f7ec57f0524a81125b059327cf367ea1f3387b48c3f642bddc82b9 in / 
# Tue, 12 Sep 2023 04:45:09 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 01:51:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac93ca815ee057f1083e81c9edcf7787c1047a557a07ded971abbb05fa515ca0`  
		Last Modified: Sat, 16 Sep 2023 01:55:18 GMT  
		Size: 27.5 MB (27458487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939194dd385d3eacfbb7f1bf5b9dcc18c16873f21f0cd06b02cceb11343c00ed`  
		Last Modified: Sat, 16 Sep 2023 01:55:16 GMT  
		Size: 14.3 MB (14252767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8e1239553e1d4214fc014d8343ebf58fdaec6f3d8c02336f867a7364d774ff`  
		Last Modified: Sat, 16 Sep 2023 01:55:31 GMT  
		Size: 45.0 MB (45012700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
