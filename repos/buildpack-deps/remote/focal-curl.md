## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:bb0c372122ff648a4aa349b044e75cbf5b679e41490460545d599a909bc9d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:94e044314758988df3dae2b6b6a28d578bc23b7b4b9c95fabf6739d76359b69c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39959134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865524822dd50cf3883e57d429bbf60dd18b634b350e9bed85e1106b50d28280`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:44:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e116ffc838f0cc3660ba0025acde46283eca99aa80f9c11e46acc54b9cdb38`  
		Last Modified: Fri, 18 Mar 2022 07:09:58 GMT  
		Size: 7.8 MB (7769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295af90e4ff2d1c9c70f7c1d5fa7237dc821ae85afe3acda9ad3ad1167c9a64`  
		Last Modified: Fri, 18 Mar 2022 07:09:57 GMT  
		Size: 3.6 MB (3624149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:08726952c7fa1a22ea52d69b3b6627b88383cceda56abea8ef3aeeeffae34d5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33941989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ccb3a8ade301bd72398217c44b85dfbd185ef8abaa297a54bfc57e200280e3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:31 GMT
ADD file:984d3d8b31abd025bb9be52f42d60245a76b1ee991f286db819ae204da45390c in / 
# Thu, 03 Mar 2022 21:21:32 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:18:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:12a77aaceb8aa1438ebb61cb4904d74fc225cfa20464a060980580674a0a31e9`  
		Last Modified: Thu, 03 Mar 2022 21:25:09 GMT  
		Size: 24.1 MB (24073718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95bbeb0964a4dfab73961fd149020ba71ce9126e727bd4bdcc3459893584bd`  
		Last Modified: Fri, 04 Mar 2022 03:37:39 GMT  
		Size: 6.8 MB (6764147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2e94ebf7c26007ac748c1e312e5eead31afe68486073db400e6e58a3d42103`  
		Last Modified: Fri, 04 Mar 2022 03:37:37 GMT  
		Size: 3.1 MB (3104124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6896bd27deb15211dade714aebb502e5597bf04d0f32c0ed1fef5e459ad36f90
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38191681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd66f8dd794a780985619d6aed00b8c68d52ba0f195c67cddbf78fda232f958`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:08:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423f6ab0d295508b63ce61e1987bff0c82460c3a08b182062c758da4dff33ad9`  
		Last Modified: Thu, 03 Mar 2022 20:17:14 GMT  
		Size: 7.6 MB (7635518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccf3179768ddeede50c028e84e91486f3fe53c57720562347abec869126f029`  
		Last Modified: Thu, 03 Mar 2022 20:17:13 GMT  
		Size: 3.4 MB (3386532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:69f09eebb16093893042b07e0ef40c3d8e145ef17e996e2ad48f24fb5ed873ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46472266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e6813de8f1b6918d3c45291945fd72d29233f10bb419de92bec40e27ecef3b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:30 GMT
ADD file:039f04ac6c5dbbe3fb0a5eee16945cf7c5fb7565751d6bdf8ec0c1102798c1de in / 
# Thu, 03 Mar 2022 20:28:38 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:23:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a16b43de69d1e799ea2cb675e7e605db0ff3a8d692fd326fbde80a370e0676d5`  
		Last Modified: Thu, 03 Mar 2022 20:33:55 GMT  
		Size: 33.3 MB (33292195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e0a1b9bbd2b2b029e920fa7af6ee761ebc38994d46eaa73805fad6046369f`  
		Last Modified: Thu, 03 Mar 2022 22:01:00 GMT  
		Size: 8.7 MB (8723922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08de314573707f75376790e410ddfcfc9415f9c94c9241d04fb519be643d5f7`  
		Last Modified: Thu, 03 Mar 2022 22:00:59 GMT  
		Size: 4.5 MB (4456149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f92eb8677b50cf80d87db00924ce1af4cf1931ee4e26397f38e26cc88ba0f536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34119039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5951dc99fb934da63e2c6e5947d44d412fa0c2355325cfade887213061db7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:38:15 GMT
ADD file:efb773758373b91272f89713203d5060a7d4ba8d2483df3450dd0962daac92a0 in / 
# Fri, 18 Mar 2022 00:38:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 02:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 02:55:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6ebe5c6e93a03a169950be6b086c0881dc2b7bde18bab91909cba84376d5c894`  
		Last Modified: Fri, 18 Mar 2022 00:56:03 GMT  
		Size: 24.2 MB (24227824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a2896dab389d54a6c60c12fa24b68a123e68fa1ae83a8fcc586d64a5a57eaf`  
		Last Modified: Fri, 18 Mar 2022 03:38:04 GMT  
		Size: 6.7 MB (6746587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce654583d8cc0286ad8e8f6321c41369147309b8eff540ca84cd9e62ec2362d7`  
		Last Modified: Fri, 18 Mar 2022 03:37:59 GMT  
		Size: 3.1 MB (3144628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d9c49af03d4f44861e4752ec4e223f4cb3018a7972f67858428910cbd74dc1bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38050860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe75bd7bad45185a3bd5686c40ab26b9e1a7990e3a647e1c1f461b7fff5c9e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:07:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eaf29f2deb1458247f93d37e2ed32c08cea87fad43790f16f5dd3af910eeb9`  
		Last Modified: Fri, 18 Mar 2022 17:15:16 GMT  
		Size: 7.4 MB (7423774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e26efb63698a7b8837e6774a425a1d0c4740a7e8bbaa73cf98149c9fbe414b9`  
		Last Modified: Fri, 18 Mar 2022 17:15:16 GMT  
		Size: 3.5 MB (3542254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
