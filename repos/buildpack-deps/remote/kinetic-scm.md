## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:ec2fd98bb6a94e484b514868aaaa324090409ffcc79fcada338f21ff8b1b6b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0a8c9068c8edea1b3971550c17b5e83d42fdad70421e4c30e6453583a99cb4ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77496633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7ab602eaae747a1f031cbfe90ce88c013d501794705d98a8257df656992f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1668d3645729ae45f8050cfcb2a85fa59293b2179fee5ecc56693f1ffdc90`  
		Last Modified: Tue, 02 May 2023 23:44:26 GMT  
		Size: 10.2 MB (10190664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b935b8133c4e2eb29849d47bce84bf208d666f60c306bd03d61cf01a8dbfcca7`  
		Last Modified: Tue, 02 May 2023 23:44:40 GMT  
		Size: 39.8 MB (39823904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:051acea3cf8659dd548dd8edba03b3469c91a75eff03d5284d987e7c8f763125
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81971845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdf6a303e4b064998fd46e0ac0718e946003c4b2b722747bf89dc86e3f86adb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:05:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b920c96303573225aded058cd081e94c75571fbc105df19e26a478d711fca4`  
		Last Modified: Wed, 17 May 2023 00:25:45 GMT  
		Size: 13.1 MB (13143121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f3585b7928ddfa9f52d2ec9ce50851d1987db30ccb6b2a530ea8df27e0ace3`  
		Last Modified: Wed, 17 May 2023 00:26:01 GMT  
		Size: 42.9 MB (42937473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ab047230a05e902e860a38dc37af42986670d8173a73048ab195702d28b7768d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80066721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da151f69376d4666824d5038ae9c3a5444d0e94e1132bf5ce3354162ba7afb41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:44:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5a0c1413473bd48a6e359ce099bb9fac129bce6960ed9b6aab520bedeb023`  
		Last Modified: Tue, 16 May 2023 23:58:10 GMT  
		Size: 13.7 MB (13731869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65c3ae4b9d03220f857773c67484ef761aa2c8900bc3c999e0240e363b0a26`  
		Last Modified: Tue, 16 May 2023 23:58:22 GMT  
		Size: 39.6 MB (39632679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1926b38f336f5f0ce54ab32729074d6433c6c35006993f35d45cbd4368131cd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88215970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae896d5e276b20cb4733d2c055a1c7f5d5afb181135025e0b0490e263f65a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993aa98c961f4195af2b7f290763be0ff615ac3cfee1dc3a4f40a08e9bd697fa`  
		Last Modified: Wed, 03 May 2023 00:20:31 GMT  
		Size: 11.9 MB (11889228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9565621d5ec2164b426a318ec987412a8a6336c7b16bf68757e1b67e979faa`  
		Last Modified: Wed, 03 May 2023 00:20:53 GMT  
		Size: 44.2 MB (44228133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2f0c447228392014fb7795407dae5ae03d73e04fc377560f71e4ee92d110d773
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80059456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7585814f8fb6ae3f0df647c1198b7c5983bc51e75bc6e30859fe5b2f40b968`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:46:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f712e29cfb9c4e3fa37cc777de5ec3a547378889617b0615c8957c5af9efdc`  
		Last Modified: Tue, 16 May 2023 23:56:45 GMT  
		Size: 14.4 MB (14356745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0593c08fbad964cbc99680820860c517053213feedaf4373e92cea0004136887`  
		Last Modified: Tue, 16 May 2023 23:56:55 GMT  
		Size: 39.7 MB (39673424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
