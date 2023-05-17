## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:50a5e3604945e823e3921a8c99bdb904d9bbd2322131995afb031bee111a0a74
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
$ docker pull buildpack-deps@sha256:44f8eb9cc019f857e1e3480bf134c9e875e8e60bf03412658fbcbef9105862c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81728345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ca31773c129e63d52677257f6cd307c0d0e47d5c8752c1201f68bf8e630c1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 20:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:08:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6c6b907db42b6f1b03645d7cd822afa676930182719410e133c9480fede45d4`  
		Last Modified: Wed, 03 May 2023 16:46:32 GMT  
		Size: 27.6 MB (27604112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db8f628eadae81eed04537247fbc6272b83d4dce338e7ca875143d8702c14c0`  
		Last Modified: Wed, 03 May 2023 20:17:07 GMT  
		Size: 9.8 MB (9781500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed7b5916395be6abd3a3f41069beb08289681b448f14afdd062a8d630050805`  
		Last Modified: Wed, 03 May 2023 20:17:24 GMT  
		Size: 44.3 MB (44342733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f27658d47ae4212f9c1edbe5e24c6d4bebdfda7ef7919619e1231de48305ba72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83229177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77800e77962fb401db2a3ed04608a462bbccfe7644e2fdb5b12fcae3d76a58c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8f976bcf9a33d090294b25c3fb3430a5833ce92be9f477471addb457c0dc3ac`  
		Last Modified: Wed, 03 May 2023 22:12:58 GMT  
		Size: 25.4 MB (25437887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653ea3e4c9dbd15b264a4a6a10dddb593e3d21e899c82f1684533e0b63e3191`  
		Last Modified: Wed, 03 May 2023 22:12:56 GMT  
		Size: 9.1 MB (9103832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51bd461eaec416e884ed0c9598fa7c90d7dc6a5ce5f4cc445fcd549b5b56c38`  
		Last Modified: Wed, 03 May 2023 22:13:14 GMT  
		Size: 48.7 MB (48687458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e3d62086cb295abcc7a6411e6e5530e28e571be4459477586a99ee8b8db975d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84561257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88425b0182105a165f059adb1fc4af6629cca0f08c46b1eb24c070ba5e9a530`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eedec38ef10e1ff872f423ceae12828c5413c8183c216098c34342de77e9e5a3`  
		Last Modified: Wed, 03 May 2023 17:40:37 GMT  
		Size: 27.0 MB (27017867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b19b0b741f1c54f6a360843f1321028128af5d283a1d8f0f5f66bf8beece0a`  
		Last Modified: Tue, 16 May 2023 23:58:57 GMT  
		Size: 13.3 MB (13349536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ede9cbd1d38078a543a2cb21cdb02b9aad695324d7f312340903eed543424da`  
		Last Modified: Tue, 16 May 2023 23:59:11 GMT  
		Size: 44.2 MB (44193854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b866b42d8fe31ef90c1a8a5c626c457c8323009f2b1298bb652af5c04054a6b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92526976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4b5b17ec2d74cffe8842da53b5318f67079f5da4f3404f58fb246b8c048cc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 23:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:29:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff954998e64505d58ea7cf2bf1a248c9fdc2287c6f6c0f41d3268aa8df574bb`  
		Last Modified: Wed, 03 May 2023 23:42:18 GMT  
		Size: 32.0 MB (31996798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e392eac2e54d3ce287c6ad52608235e58697dd34630b471eb3e306bf35c2a09e`  
		Last Modified: Wed, 03 May 2023 23:42:09 GMT  
		Size: 11.5 MB (11489279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480d337a20f31a2c377c8923ba928c77b4a5ad0c78cf2c281f4ca0e3a1a98b29`  
		Last Modified: Wed, 03 May 2023 23:42:43 GMT  
		Size: 49.0 MB (49040899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:13d466e828964bc26a839bce9d6af7b5be86424794138cfb58cf68de1e44730a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84476595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06548fc41aa53dfdcbacd2708258bdb45a5e9d327b2c27f456638a6c6b26f7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:50:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e12ee780e94e13677b8efd3cfc5219f323ee331fab05eb1f1c59218a106122b`  
		Last Modified: Wed, 03 May 2023 22:34:25 GMT  
		Size: 26.2 MB (26236160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc738121c9813521fa4a0fca88e02cb1f66ef200380dff38dd077ab483e2c4b`  
		Last Modified: Tue, 16 May 2023 23:57:26 GMT  
		Size: 14.0 MB (14017600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b0c0328488d708fd92c4400fc82d0ff82947be475b2cec1e956ce34dcb9057`  
		Last Modified: Tue, 16 May 2023 23:57:37 GMT  
		Size: 44.2 MB (44222835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
