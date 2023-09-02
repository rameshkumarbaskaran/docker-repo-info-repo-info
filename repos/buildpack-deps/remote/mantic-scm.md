## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:250925e13515ab5fc72ec4a801e1ed70ddc5a0da1e67e676e14a747b1ab71d5e
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
$ docker pull buildpack-deps@sha256:f1758069423c18f1d2a53b15b07d176b308d0f9638ab8a341d5b3664d03f1dad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94121578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c54b8c1116b61354aa3da83ee578fb5023abc99f8611bb09e421976e8abff0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:04:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:04:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:04:55 GMT
ADD file:87bbd4b1a17b5a9990befc7d85a50c9b813d3cea95c9f28e0001a40d6b7deaf4 in / 
# Sat, 19 Aug 2023 05:04:56 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:07:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:08:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:717fa18fb0fc884d9a94c702c32647885b210c59e1fa77ea32995b51deb76537`  
		Last Modified: Sat, 02 Sep 2023 00:07:33 GMT  
		Size: 27.9 MB (27898869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84652230bf87528d3bcfe5fe4fef2e3d3e197372d5eb30e3cd0952ca6feea84`  
		Last Modified: Sat, 02 Sep 2023 00:13:47 GMT  
		Size: 20.0 MB (20033729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d0466e4a84f6b282e06c9695d238afb6a05f5436661d460a6f4cb395921606`  
		Last Modified: Sat, 02 Sep 2023 00:14:02 GMT  
		Size: 46.2 MB (46188980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:de6e17a83b3432ccde1604364752699b4eadb721fbc77b3dd5caf056e92c934c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93301258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa927f0daef47031ac1092ed6424ee9df4131e09a94a53123f76fc9281f5e5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:05:42 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:05:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:05:47 GMT
ADD file:b2556a8208f666e3c07a759d0acbc23841ac60abc72026ca23e8a2d2c96a3c9e in / 
# Sat, 19 Aug 2023 05:05:47 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:51:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b202a4ddab8fff273b81c7544dcb792ca7858b4cd7cdcd12e551f3d5382b8f10`  
		Last Modified: Fri, 01 Sep 2023 23:56:33 GMT  
		Size: 25.5 MB (25452732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7ec094154d11eaf24d03d379c6aab843118a05535d0377edf88e33135e4cbb`  
		Last Modified: Fri, 01 Sep 2023 23:56:31 GMT  
		Size: 17.6 MB (17596155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75352c292c46da0ffb27109cc56e769c3433ba90f9f5aa092cbdaeddfca30c5f`  
		Last Modified: Fri, 01 Sep 2023 23:56:48 GMT  
		Size: 50.3 MB (50252371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5b632bd358f1b045135d156f53cf7349e7b3311400d67e0f3fcfa8b68d91055
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92440850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031ab4026ed45e324f841017f051a000f86ada7aa43e8cf3a52cc51b0db118c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:09:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:09:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:10:02 GMT
ADD file:cc6a3e0225d3c4171348881d7482651292156aeaaee88bc0ed81e8a850fe21f7 in / 
# Sat, 19 Aug 2023 05:10:03 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:21:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7ad6503180330babb207079119820c257dd6aa2275b3a0e8e507fa5535e83de`  
		Last Modified: Fri, 01 Sep 2023 23:27:40 GMT  
		Size: 27.3 MB (27264110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58883c3667ca078a9f47c68653ab34ee1d76f9c3bf1869cfa801b1bbd1f8af16`  
		Last Modified: Fri, 01 Sep 2023 23:27:39 GMT  
		Size: 19.2 MB (19228183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff4bfaffc5bb4a3e10976d79e4dfe9200424f4be3b30fbc6c6beaf5fbbac5b6`  
		Last Modified: Fri, 01 Sep 2023 23:27:53 GMT  
		Size: 45.9 MB (45948557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b549c7d7169d317ce7e0e294ac22f3dfba3f04673f410bb38dc6075cfc6a9a66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106127395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5bec2abb3cde844693a5d6c22df198ab39e17a67cd032986a0448b911b62a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:08:05 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:08:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:08:08 GMT
ADD file:e4a36c75d3f498442e29bc6100bb11ebebbc8ba67e315acb43bc0ad4a1d1421a in / 
# Sat, 19 Aug 2023 05:08:08 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:04:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:502f153255845f7a71eab15b26114f05bab81e3c3e9097088072dfcf63d71724`  
		Last Modified: Sat, 02 Sep 2023 01:15:49 GMT  
		Size: 32.2 MB (32235872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b369d7b0190fa57d85fd8b0f7e7b42aadc96f54c307a2a515511d95ca268df`  
		Last Modified: Sat, 02 Sep 2023 01:15:46 GMT  
		Size: 22.8 MB (22817405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb21a0f141657d72e70094e8676c2bb0da469e64e216f3ebf8d473a09806c05`  
		Last Modified: Sat, 02 Sep 2023 01:16:14 GMT  
		Size: 51.1 MB (51074118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:39083b5f214b26a57f519ddd9ca7859afa21ca88ccd8920d5bc8e7633d3082be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7af2798866d99ecca5f843d9237a5aa7e1234de8473978a38d9859aea6544b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:07:37 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:07:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:07:39 GMT
ADD file:681bda53818a2c0f492a5b6c8f35eb4ecba1d81c3c51e02310824c03db9146e6 in / 
# Sat, 19 Aug 2023 05:07:39 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b09de31f2a7e0477e15ccd77e26be0df5df0f755bea2d6bb52236401d3e3684a`  
		Last Modified: Fri, 01 Sep 2023 23:24:59 GMT  
		Size: 26.9 MB (26936780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d5be6eaee2b4edf324dac730d3dc0afca32176b2dd3c65d0705af55ab42a00`  
		Last Modified: Fri, 01 Sep 2023 23:24:57 GMT  
		Size: 19.5 MB (19502292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17bacc9d32f9c9fbbe2742619bbdc5319125f09d50a550996f882259886d577`  
		Last Modified: Fri, 01 Sep 2023 23:25:15 GMT  
		Size: 46.4 MB (46421679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
