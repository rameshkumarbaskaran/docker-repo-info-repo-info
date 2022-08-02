## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:8b426026fcb8ad799f55534d66302199573adafec76dd3bc8b5da85279b0593b
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
$ docker pull buildpack-deps@sha256:b878485ec2477b01b4f030e41259bcf75dfa7565e34da98cbcbcc72664f2e3c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100696152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c77f89365fbb7f1cf52c8da0201f4eac537fc52a0f2c55779869f004598c8a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 02:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:07:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 07 Jun 2022 02:08:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0b6a9c72470ff5d8860f27875472d3ad0d4b19051144f27660ad480b70c73c`  
		Last Modified: Tue, 07 Jun 2022 02:24:50 GMT  
		Size: 7.8 MB (7768843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27bf6512b10b479ce26a5fccce481830b0b356e00838901ed5d1d051119e3f6`  
		Last Modified: Tue, 07 Jun 2022 02:24:50 GMT  
		Size: 3.6 MB (3624431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc5331f186f0258321175753c071842d764a2bb5d9ebfcfd39cbfb6b96bc9bd`  
		Last Modified: Tue, 07 Jun 2022 02:25:10 GMT  
		Size: 60.7 MB (60730246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:506ca4dc0fe18862daa9d58e6a14bb9f887c89cc4ef02bfb47ce56ec78092c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90085921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422c49fd6f50393949c47cda4edc7930dca24a89394d11dfa846d4a0330e7445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:37:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:37:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 28 Jul 2022 13:38:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bbc4b5cf692ef2c4a6d823bf539a7ea8860610a4b13785e87d2e31088bde7b`  
		Last Modified: Thu, 28 Jul 2022 14:00:41 GMT  
		Size: 6.8 MB (6756448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ecd77d6d00f7dde6dbbe6619f7b2de7e53ad92bf88494636b6addfc2d5ceae`  
		Last Modified: Thu, 28 Jul 2022 14:00:39 GMT  
		Size: 3.3 MB (3295499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de98a0739d2dde5e0d055993d91c3f95dbb321c6e4d8964dadc963165373f7b9`  
		Last Modified: Thu, 28 Jul 2022 14:01:14 GMT  
		Size: 55.4 MB (55441335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b71a8906806c99ef88b8041f9a45e0afe2acd7009a552f9c81dc23e4ca3e4af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99019642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8566bb72845bcff4317f7fd0c54d0526604721d3f6a070d8e35ba0ca39408bf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:32:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:33:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444542145972df20962fba6d4329459e66f2f686af24d63dafc2c5a1b6efe52`  
		Last Modified: Tue, 02 Aug 2022 01:49:44 GMT  
		Size: 7.6 MB (7631155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9924b49b3caa4a90a845795499c127cec28b1a834dea8b2af26a4a464f5cdfed`  
		Last Modified: Tue, 02 Aug 2022 01:49:43 GMT  
		Size: 3.4 MB (3387837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed573e2ecfd9cbbaf3a2a9731cf671288e88bd6d11779c78cd1d5995014da6f`  
		Last Modified: Tue, 02 Aug 2022 01:50:05 GMT  
		Size: 60.8 MB (60808846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:15310b8219a2872d7a7e7fb3182408e0b733cffe02c4365fa03e8d47e3a3be62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116298219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881fb8ec687060226d21dffcd2ca2aa4a60c6f35ca70f7849f1aa7d314d7641f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:02 GMT
ADD file:86506a94b834ba2b6f10dc0d1955bee539be1cf565e4ccc2c4bc074e0375f115 in / 
# Tue, 07 Jun 2022 05:46:06 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:39:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 23:06:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f52d061d2d3fdde0d3a099bbeae64080476c9650e9f3ba05de898d5bb5f03e8`  
		Last Modified: Tue, 07 Jun 2022 05:49:10 GMT  
		Size: 33.3 MB (33294345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18349e42cb7ce91a943fbc86a6f7e492601f8eadea7475791a50b18ed0b9ba71`  
		Last Modified: Tue, 26 Jul 2022 23:55:25 GMT  
		Size: 8.7 MB (8719317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954ef68d2e65b1a1eb4a527b2cc3d633d76aff137ee63ecfcdbb1cc9f986f4d1`  
		Last Modified: Tue, 26 Jul 2022 23:55:24 GMT  
		Size: 4.8 MB (4754804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0a32faa32a8b78dc3fa911895e210633b01852fd3b8a7413b89758a863455e`  
		Last Modified: Tue, 26 Jul 2022 23:55:56 GMT  
		Size: 69.5 MB (69529753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7f58b3b1078c2ddd51050224fb665d95442bc51ae67427f7fccc8c9eee296012
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98009573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f9d3a3260cead7a73de251d5d9287466be51f36f5d6fcc0a5f9b4d85eae69b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:19:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:20:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afb2f7de67ad545f5de8adfd96f7578e1d0e55e79f41f3a7278650d9408712`  
		Last Modified: Tue, 02 Aug 2022 01:38:50 GMT  
		Size: 7.4 MB (7412554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67acf8da821182b10d1d774808bb08ce2cf3de1b28764bb20bb702984a97f18a`  
		Last Modified: Tue, 02 Aug 2022 01:38:50 GMT  
		Size: 3.5 MB (3542609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64595ec9f7fe9034a2c68ef3b31e56f311a8fe519da1e53b7afd841af459ae0`  
		Last Modified: Tue, 02 Aug 2022 01:39:06 GMT  
		Size: 60.0 MB (60009047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
