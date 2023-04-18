## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:8ac2d3c90924410e99481cf1f88c25d07e29052c1201befe03e9bec8c8760b26
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
$ docker pull buildpack-deps@sha256:8c474a27635a29ce1f6daffda32528a0aa48b6f589ecf88490b158f33a571f15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82127733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b46a0d94344b399c5d7604309d08fcd4a61f68a8911fd92690bd5f4a46d9c8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 18:21:45 GMT
ARG RELEASE
# Tue, 14 Mar 2023 18:21:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 18:21:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 18:21:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 18:21:47 GMT
ADD file:108000e07d9734743bfe65381248aa7e309283bdb87d8687b7ffe0d697487109 in / 
# Tue, 14 Mar 2023 18:21:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:37:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:37:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:37:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dbd9104be902889dc21019a0f5023f798f3d4659871b7eff4e60ea6f1496df08`  
		Last Modified: Thu, 16 Mar 2023 05:45:13 GMT  
		Size: 27.5 MB (27533123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f926546ac77ef389dea10f2f48a9435499b9fd85ce007f054787873fba3ba820`  
		Last Modified: Thu, 16 Mar 2023 05:45:10 GMT  
		Size: 6.7 MB (6653872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02fdac0efdc0f5d71c45d6ab71b8cf2421156adfbe3dd6673c198b60f5e696`  
		Last Modified: Thu, 16 Mar 2023 05:45:09 GMT  
		Size: 3.7 MB (3689653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57775961ac4b5f4df9ba21c9a454eec60eced52106a9c3c6480abe04fd31e975`  
		Last Modified: Thu, 16 Mar 2023 05:45:29 GMT  
		Size: 44.3 MB (44251085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b08244e2bc4db9fd4a22095b42d9044de738c27f0c4f78a9fd1303fb5e9459e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83364676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad34d38cd21a977e6a4b1485518ff8873988b314b13cb4796e11b2ed4ec4d693`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 18:18:28 GMT
ARG RELEASE
# Tue, 14 Mar 2023 18:18:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 18:18:28 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 18:18:30 GMT
ADD file:dc39df38ee577fc1ddb753815787f9a90231d34a28c65e14298d136132c8d7d5 in / 
# Tue, 14 Mar 2023 18:18:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:01:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:01:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:02:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2e2ff6a76c080ab34fadea2f47efdf4e1606b1482ed2e4597e51810a467b28a`  
		Last Modified: Thu, 16 Mar 2023 04:11:42 GMT  
		Size: 25.4 MB (25359548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003fc5922aae3f4274356fca42181568c983c95440b266598d0a8b3307f981b3`  
		Last Modified: Thu, 16 Mar 2023 04:11:39 GMT  
		Size: 5.8 MB (5819049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f573392ff6ba3d538b9dd78eaac78c3a48a8719f2c3a366e5031c24433553af7`  
		Last Modified: Thu, 16 Mar 2023 04:11:39 GMT  
		Size: 3.9 MB (3850947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e5edf4553807d09a5e079189ad8abe94fa20ac8d3b91a1fdee74ffbbfc465a`  
		Last Modified: Thu, 16 Mar 2023 04:12:00 GMT  
		Size: 48.3 MB (48335132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7718090c669d397351860cb0345fd87226c3f44bfc63156d13b88ee8b6bb13c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81133371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794f72335c8bb0cbfaa191b6c8873dca8c9aeca030e74c1f1e6e88e9df6cfe91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Mar 2023 17:38:32 GMT
ARG RELEASE
# Tue, 14 Mar 2023 17:38:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Mar 2023 17:38:32 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 14 Mar 2023 17:38:40 GMT
ADD file:2562122b72f2bcdd0678a1bd0836dcbf376a8e33078452497d85ed0cd425391f in / 
# Tue, 14 Mar 2023 17:38:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:17:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5bd94ab779df0c538759342d8eef230b315e98979bcac4604e94fb874397461b`  
		Last Modified: Thu, 16 Mar 2023 04:25:04 GMT  
		Size: 26.9 MB (26945660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df8402fa00c99b6f8233d0c6452e59cfe2742b9b2c9f44a504aaa45a0516cd3`  
		Last Modified: Thu, 16 Mar 2023 04:25:01 GMT  
		Size: 6.5 MB (6484575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa45039d5b2736a9624493cbbbf9200c134de7ddb8696ce87c68dad417e12f4`  
		Last Modified: Thu, 16 Mar 2023 04:25:01 GMT  
		Size: 3.6 MB (3648517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5195e2054b68f924f77b2db71706b518fdc87c9c6f3d900adad8e6eec601fb`  
		Last Modified: Thu, 16 Mar 2023 04:25:18 GMT  
		Size: 44.1 MB (44054619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd6a50b6a6df0aaae7eecf4f25a23d66698a56a420fceac58859c82334c373c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92720367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2680105e7ba022355f1f320347591ffcaa718b8d1c7fb525bcbaa2bd1de940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:712fd37daa58220b07ef60020b33ade10599163dc40e476600099c7058b75bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80068156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc83d080597d0511ef668ef12d04f8965d989d28c0896a33c9d5b0b3c59593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
