<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20230126`](#ubuntubionic-20230126)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230126`](#ubuntufocal-20230126)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230126`](#ubuntujammy-20230126)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230126`](#ubuntukinetic-20230126)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230128`](#ubuntulunar-20230128)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:a3765b4d74747b5e9bdd03205b3fbc4fa19a02781c185f97f24c8f4f84ed7bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:fdd3c9372c19afa928f99afde58f0f80a008ebb695a8c5ee37de5adb7feb46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2df19066aca89df8e5317544a1cb599dc657830184762ff6fdefaaf708db65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72d9f18d70f395ff9bfae4d193077ccea3ca583e3da3dd66f5c84520c0100727`  
		Last Modified: Thu, 26 Jan 2023 10:11:57 GMT  
		Size: 25.7 MB (25688613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f21972d048d5439834187f47e9e2869e5434a3c5d49f7ef721d3d5f62fe7de60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e780dbbcb4f0f3439981b5f09c45d9de103ca383942edbb8842911f2402fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:369d14bd01c8ad4c81698d2f4605509a9985da47b51206c612ebb49191c0eddd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22711894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b37ee8ce31e197fba06b7de0b4b07a6fe33e5921918be8d7e1de7b8f25893b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c2a5dda1e2b0d861ec46a9c576c4fd4d667c56aa4b1cac9cd8c16e629dd11b28`  
		Last Modified: Thu, 26 Jan 2023 10:12:11 GMT  
		Size: 22.7 MB (22711894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:fcebd6734dcbffd0c328771b11a0d00a8045f58ee5d3e083d3afdb54c72dab8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26096513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97151d96f64f3b5b7cdb0fadb1c1f8556552cedf32154f23efd48595efabb1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da6bd15c918442485ea09b9b4a679ccddef764b03c04a94fa2f0ee75bf9ae709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29351018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e533a2e815a6606d93392dd9f8ff6938a39080b67cfd575045cfe820ede7af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c790564dfb49a61552a6e89c63c7abf84177d16d0f0fb604df022bfcdc6497b`  
		Last Modified: Thu, 26 Jan 2023 10:12:31 GMT  
		Size: 29.4 MB (29351018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:2d4e5c5d55c699a3f9bcf998e7913534bc2cc9795f24be7251aef08615e04698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24744933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81833e90b6b40072356a6b1256c20d690401c5130f58b3343b6e30c2eccb64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:41 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:43 GMT
ADD file:04d4137c9183cee18560fc26a092e288ff403f3dde266237eab245bd38eb9b3a in / 
# Thu, 26 Jan 2023 09:55:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9e75830a8e632695dde0b55ec0159bd7b141ab79858367e3f66bfa5f255aaec9`  
		Last Modified: Thu, 26 Jan 2023 10:12:37 GMT  
		Size: 24.7 MB (24744933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:4a45212e9518f35983a976eead0de5eecc555a2f047134e9dd2cfc589076a00d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:bffb6799d706144f263f4b91e1226745ffb5643ea0ea89c2f709208e8d70c999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cf56b4be35b04f620bc9cfbef80038fd7370d4ed36d90676223174ecbf0b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b549f31133a955f68f9fa0d93f18436c4a180e12184b999a8ecf14f7eaa83309`  
		Last Modified: Wed, 01 Feb 2023 12:05:25 GMT  
		Size: 27.5 MB (27503418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7bb60f92af1f5062f83b4b0edd5710332e20e1f99ae6c294d8b5bd7d7551a41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2238f5e875d6e7d6f10729c620de133ae54eb25518994fcf012e02df6ec9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:363362dbf1847a398cc45b6a5f85ddbc7c633b43b9120f06e1e8cdd10237325a`  
		Last Modified: Wed, 01 Feb 2023 12:05:37 GMT  
		Size: 23.6 MB (23608452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bf9913320006dfc72a4b519ce600a4063529d242ff5b78facb2bc43ce91260d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb527b091d53464371291e6470289f0b4f9aab431da2da2ed35e43149bab2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:455c32d33260eab99dd1b8abd1c2af91801c5a580a50e7a43c60b637a88a2209`  
		Last Modified: Wed, 01 Feb 2023 12:05:31 GMT  
		Size: 26.0 MB (25972163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e66e5d8f6f3761ce46b82a167ec4b091e87f0e0902d302b4fb9781f421e9ad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a648e725100f70f48b2ca60e75e69b4b5e2a7a9abbceba82f43764bc32ca9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:210cd7d37ec304813e8c7a2036ca7ca250cda0516fe48a4139b60c4cb817eaaf`  
		Last Modified: Wed, 01 Feb 2023 12:05:43 GMT  
		Size: 32.1 MB (32068234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:95dbe0b494a2624bb9e354862de2aae054edadad8ecb7e324a266d500e727b33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8b74e1fbfe9b5f7ce7337f13fed5a604bf3af8864bed462aa60c53b64790ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 12:00:21 GMT
ARG RELEASE
# Wed, 01 Feb 2023 12:00:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 12:00:23 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Wed, 01 Feb 2023 12:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:efe4f2ca2c9f0566845f1d0abee56925904cd0a37a97cb9ccbc3f73b5cea8bcf`  
		Last Modified: Wed, 01 Feb 2023 12:05:49 GMT  
		Size: 26.4 MB (26363789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:9a0bdde4188b896a372804be2384015e90e3f84906b750c1a53539b585fbbe7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:61bd0b97000996232eb07b8d0e9375d14197f78aa850c2506417ef995a7199a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27342387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be1f66f70f66ef43503292e38ccbfc14f2d5464e7736344783a8fc7bb339a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b150fd943bcd54ef788cece17523d19031f745b099a798de65247900d102e18`  
		Last Modified: Thu, 26 Jan 2023 05:14:03 GMT  
		Size: 27.3 MB (27342387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:226ce9ec935d4ae0207fd3c9d44b8edd62302a528ee66c5adb39f7ac5b8a0993
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28009396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbed079020c533dbc7ca626067d743bf7effce2e4c895f104846afd8f4943a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f8e318d098424cef87513f4c834987f20c608791646c6b1a3ef60ed57408ddb6`  
		Last Modified: Thu, 26 Jan 2023 05:14:22 GMT  
		Size: 28.0 MB (28009396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:a630e0fd2ea08f74080cddba4063fb9a840526697c551f52a183c674e3130179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dae786ed48a53dd5568147addd2a80c41f7576823e0cba466c5520003a169ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7096432b6a9855592152ad8009431b92d7aa40980c9c94684fcc72626bbbab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:05f69cab0b799028e03233ffa93abd2d0b426412cff70959a07a29a437447ee3`  
		Last Modified: Thu, 26 Jan 2023 12:14:10 GMT  
		Size: 25.8 MB (25757647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:c4b1f492c91d866555c6eb6335660e39fa7153eb4aecb19e4f4893d580d14a3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91297aceb6d3e297e45ec91916dbea079b90ae1c7edbaf14a99c41d3f493f537`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe4914a812d394969d56f220e5ddb037a62164607a937ca866bf4ee592a8799a`  
		Last Modified: Thu, 26 Jan 2023 12:14:28 GMT  
		Size: 25.5 MB (25487159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:678c136e4e918eff1c5e83383859e1ea2227d75ae5fe662c9122711aa6594a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0c8e3367a3fe9b703c759e1c148c5809df1a2734f8f37529bd11fbcfd34b1d1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d2fb228861107934403e776544a3f516bc7123a1275d52f1992bada8e94d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:24 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:29 GMT
ADD file:c6e9b4142d0eef696dbc592460bdbd505f41a98d02ba1c7a84caedbb5f84ea1b in / 
# Sat, 28 Jan 2023 05:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29d183ded65aecf549f39ef891c21feb9034b5b10f341533b4af297bb5c60bb8`  
		Last Modified: Sat, 28 Jan 2023 05:21:31 GMT  
		Size: 25.8 MB (25802344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:af9488f1c2d5b6b3d0052c1bba305d8d532dea8c909a67bf8e4ab80fb941eaef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25486743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a9b2f2593848f8bbbfe35751460fdc9625ad88582cd228a1b8a6ae5fd1159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:10:10 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:10:12 GMT
ADD file:b85f8b675931991dc4361ad29563c508e8cdd381491f1da64b998d7742f72c42 in / 
# Sat, 28 Jan 2023 05:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24a981375fc3c6ae016cae56fbf42f85436ada457d63c95255694c34e6f336a4`  
		Last Modified: Sat, 28 Jan 2023 05:21:50 GMT  
		Size: 25.5 MB (25486743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:a3765b4d74747b5e9bdd03205b3fbc4fa19a02781c185f97f24c8f4f84ed7bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:fdd3c9372c19afa928f99afde58f0f80a008ebb695a8c5ee37de5adb7feb46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2df19066aca89df8e5317544a1cb599dc657830184762ff6fdefaaf708db65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72d9f18d70f395ff9bfae4d193077ccea3ca583e3da3dd66f5c84520c0100727`  
		Last Modified: Thu, 26 Jan 2023 10:11:57 GMT  
		Size: 25.7 MB (25688613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f21972d048d5439834187f47e9e2869e5434a3c5d49f7ef721d3d5f62fe7de60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e780dbbcb4f0f3439981b5f09c45d9de103ca383942edbb8842911f2402fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:369d14bd01c8ad4c81698d2f4605509a9985da47b51206c612ebb49191c0eddd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22711894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b37ee8ce31e197fba06b7de0b4b07a6fe33e5921918be8d7e1de7b8f25893b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c2a5dda1e2b0d861ec46a9c576c4fd4d667c56aa4b1cac9cd8c16e629dd11b28`  
		Last Modified: Thu, 26 Jan 2023 10:12:11 GMT  
		Size: 22.7 MB (22711894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:fcebd6734dcbffd0c328771b11a0d00a8045f58ee5d3e083d3afdb54c72dab8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26096513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97151d96f64f3b5b7cdb0fadb1c1f8556552cedf32154f23efd48595efabb1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da6bd15c918442485ea09b9b4a679ccddef764b03c04a94fa2f0ee75bf9ae709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29351018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e533a2e815a6606d93392dd9f8ff6938a39080b67cfd575045cfe820ede7af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c790564dfb49a61552a6e89c63c7abf84177d16d0f0fb604df022bfcdc6497b`  
		Last Modified: Thu, 26 Jan 2023 10:12:31 GMT  
		Size: 29.4 MB (29351018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:2d4e5c5d55c699a3f9bcf998e7913534bc2cc9795f24be7251aef08615e04698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24744933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81833e90b6b40072356a6b1256c20d690401c5130f58b3343b6e30c2eccb64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:41 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:43 GMT
ADD file:04d4137c9183cee18560fc26a092e288ff403f3dde266237eab245bd38eb9b3a in / 
# Thu, 26 Jan 2023 09:55:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9e75830a8e632695dde0b55ec0159bd7b141ab79858367e3f66bfa5f255aaec9`  
		Last Modified: Thu, 26 Jan 2023 10:12:37 GMT  
		Size: 24.7 MB (24744933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic-20230126`

```console
$ docker pull ubuntu@sha256:a3765b4d74747b5e9bdd03205b3fbc4fa19a02781c185f97f24c8f4f84ed7bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20230126` - linux; amd64

```console
$ docker pull ubuntu@sha256:fdd3c9372c19afa928f99afde58f0f80a008ebb695a8c5ee37de5adb7feb46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2df19066aca89df8e5317544a1cb599dc657830184762ff6fdefaaf708db65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72d9f18d70f395ff9bfae4d193077ccea3ca583e3da3dd66f5c84520c0100727`  
		Last Modified: Thu, 26 Jan 2023 10:11:57 GMT  
		Size: 25.7 MB (25688613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230126` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f21972d048d5439834187f47e9e2869e5434a3c5d49f7ef721d3d5f62fe7de60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e780dbbcb4f0f3439981b5f09c45d9de103ca383942edbb8842911f2402fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230126` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:369d14bd01c8ad4c81698d2f4605509a9985da47b51206c612ebb49191c0eddd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22711894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b37ee8ce31e197fba06b7de0b4b07a6fe33e5921918be8d7e1de7b8f25893b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c2a5dda1e2b0d861ec46a9c576c4fd4d667c56aa4b1cac9cd8c16e629dd11b28`  
		Last Modified: Thu, 26 Jan 2023 10:12:11 GMT  
		Size: 22.7 MB (22711894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230126` - linux; 386

```console
$ docker pull ubuntu@sha256:fcebd6734dcbffd0c328771b11a0d00a8045f58ee5d3e083d3afdb54c72dab8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26096513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97151d96f64f3b5b7cdb0fadb1c1f8556552cedf32154f23efd48595efabb1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230126` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da6bd15c918442485ea09b9b4a679ccddef764b03c04a94fa2f0ee75bf9ae709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29351018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e533a2e815a6606d93392dd9f8ff6938a39080b67cfd575045cfe820ede7af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c790564dfb49a61552a6e89c63c7abf84177d16d0f0fb604df022bfcdc6497b`  
		Last Modified: Thu, 26 Jan 2023 10:12:31 GMT  
		Size: 29.4 MB (29351018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230126` - linux; s390x

```console
$ docker pull ubuntu@sha256:2d4e5c5d55c699a3f9bcf998e7913534bc2cc9795f24be7251aef08615e04698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24744933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81833e90b6b40072356a6b1256c20d690401c5130f58b3343b6e30c2eccb64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:41 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:43 GMT
ADD file:04d4137c9183cee18560fc26a092e288ff403f3dde266237eab245bd38eb9b3a in / 
# Thu, 26 Jan 2023 09:55:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9e75830a8e632695dde0b55ec0159bd7b141ab79858367e3f66bfa5f255aaec9`  
		Last Modified: Thu, 26 Jan 2023 10:12:37 GMT  
		Size: 24.7 MB (24744933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:678c136e4e918eff1c5e83383859e1ea2227d75ae5fe662c9122711aa6594a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0c8e3367a3fe9b703c759e1c148c5809df1a2734f8f37529bd11fbcfd34b1d1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d2fb228861107934403e776544a3f516bc7123a1275d52f1992bada8e94d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:24 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:29 GMT
ADD file:c6e9b4142d0eef696dbc592460bdbd505f41a98d02ba1c7a84caedbb5f84ea1b in / 
# Sat, 28 Jan 2023 05:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29d183ded65aecf549f39ef891c21feb9034b5b10f341533b4af297bb5c60bb8`  
		Last Modified: Sat, 28 Jan 2023 05:21:31 GMT  
		Size: 25.8 MB (25802344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:af9488f1c2d5b6b3d0052c1bba305d8d532dea8c909a67bf8e4ab80fb941eaef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25486743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a9b2f2593848f8bbbfe35751460fdc9625ad88582cd228a1b8a6ae5fd1159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:10:10 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:10:12 GMT
ADD file:b85f8b675931991dc4361ad29563c508e8cdd381491f1da64b998d7742f72c42 in / 
# Sat, 28 Jan 2023 05:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24a981375fc3c6ae016cae56fbf42f85436ada457d63c95255694c34e6f336a4`  
		Last Modified: Sat, 28 Jan 2023 05:21:50 GMT  
		Size: 25.5 MB (25486743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:4a45212e9518f35983a976eead0de5eecc555a2f047134e9dd2cfc589076a00d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:bffb6799d706144f263f4b91e1226745ffb5643ea0ea89c2f709208e8d70c999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cf56b4be35b04f620bc9cfbef80038fd7370d4ed36d90676223174ecbf0b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b549f31133a955f68f9fa0d93f18436c4a180e12184b999a8ecf14f7eaa83309`  
		Last Modified: Wed, 01 Feb 2023 12:05:25 GMT  
		Size: 27.5 MB (27503418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7bb60f92af1f5062f83b4b0edd5710332e20e1f99ae6c294d8b5bd7d7551a41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2238f5e875d6e7d6f10729c620de133ae54eb25518994fcf012e02df6ec9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:363362dbf1847a398cc45b6a5f85ddbc7c633b43b9120f06e1e8cdd10237325a`  
		Last Modified: Wed, 01 Feb 2023 12:05:37 GMT  
		Size: 23.6 MB (23608452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bf9913320006dfc72a4b519ce600a4063529d242ff5b78facb2bc43ce91260d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb527b091d53464371291e6470289f0b4f9aab431da2da2ed35e43149bab2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:455c32d33260eab99dd1b8abd1c2af91801c5a580a50e7a43c60b637a88a2209`  
		Last Modified: Wed, 01 Feb 2023 12:05:31 GMT  
		Size: 26.0 MB (25972163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e66e5d8f6f3761ce46b82a167ec4b091e87f0e0902d302b4fb9781f421e9ad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a648e725100f70f48b2ca60e75e69b4b5e2a7a9abbceba82f43764bc32ca9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:210cd7d37ec304813e8c7a2036ca7ca250cda0516fe48a4139b60c4cb817eaaf`  
		Last Modified: Wed, 01 Feb 2023 12:05:43 GMT  
		Size: 32.1 MB (32068234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:95dbe0b494a2624bb9e354862de2aae054edadad8ecb7e324a266d500e727b33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8b74e1fbfe9b5f7ce7337f13fed5a604bf3af8864bed462aa60c53b64790ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 12:00:21 GMT
ARG RELEASE
# Wed, 01 Feb 2023 12:00:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 12:00:23 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Wed, 01 Feb 2023 12:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:efe4f2ca2c9f0566845f1d0abee56925904cd0a37a97cb9ccbc3f73b5cea8bcf`  
		Last Modified: Wed, 01 Feb 2023 12:05:49 GMT  
		Size: 26.4 MB (26363789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230126`

```console
$ docker pull ubuntu@sha256:4a45212e9518f35983a976eead0de5eecc555a2f047134e9dd2cfc589076a00d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230126` - linux; amd64

```console
$ docker pull ubuntu@sha256:bffb6799d706144f263f4b91e1226745ffb5643ea0ea89c2f709208e8d70c999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cf56b4be35b04f620bc9cfbef80038fd7370d4ed36d90676223174ecbf0b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b549f31133a955f68f9fa0d93f18436c4a180e12184b999a8ecf14f7eaa83309`  
		Last Modified: Wed, 01 Feb 2023 12:05:25 GMT  
		Size: 27.5 MB (27503418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230126` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7bb60f92af1f5062f83b4b0edd5710332e20e1f99ae6c294d8b5bd7d7551a41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2238f5e875d6e7d6f10729c620de133ae54eb25518994fcf012e02df6ec9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:363362dbf1847a398cc45b6a5f85ddbc7c633b43b9120f06e1e8cdd10237325a`  
		Last Modified: Wed, 01 Feb 2023 12:05:37 GMT  
		Size: 23.6 MB (23608452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230126` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bf9913320006dfc72a4b519ce600a4063529d242ff5b78facb2bc43ce91260d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb527b091d53464371291e6470289f0b4f9aab431da2da2ed35e43149bab2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:455c32d33260eab99dd1b8abd1c2af91801c5a580a50e7a43c60b637a88a2209`  
		Last Modified: Wed, 01 Feb 2023 12:05:31 GMT  
		Size: 26.0 MB (25972163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230126` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e66e5d8f6f3761ce46b82a167ec4b091e87f0e0902d302b4fb9781f421e9ad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a648e725100f70f48b2ca60e75e69b4b5e2a7a9abbceba82f43764bc32ca9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:210cd7d37ec304813e8c7a2036ca7ca250cda0516fe48a4139b60c4cb817eaaf`  
		Last Modified: Wed, 01 Feb 2023 12:05:43 GMT  
		Size: 32.1 MB (32068234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230126` - linux; s390x

```console
$ docker pull ubuntu@sha256:95dbe0b494a2624bb9e354862de2aae054edadad8ecb7e324a266d500e727b33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8b74e1fbfe9b5f7ce7337f13fed5a604bf3af8864bed462aa60c53b64790ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 12:00:21 GMT
ARG RELEASE
# Wed, 01 Feb 2023 12:00:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 12:00:23 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Wed, 01 Feb 2023 12:00:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:efe4f2ca2c9f0566845f1d0abee56925904cd0a37a97cb9ccbc3f73b5cea8bcf`  
		Last Modified: Wed, 01 Feb 2023 12:05:49 GMT  
		Size: 26.4 MB (26363789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:9a0bdde4188b896a372804be2384015e90e3f84906b750c1a53539b585fbbe7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:61bd0b97000996232eb07b8d0e9375d14197f78aa850c2506417ef995a7199a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27342387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be1f66f70f66ef43503292e38ccbfc14f2d5464e7736344783a8fc7bb339a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b150fd943bcd54ef788cece17523d19031f745b099a798de65247900d102e18`  
		Last Modified: Thu, 26 Jan 2023 05:14:03 GMT  
		Size: 27.3 MB (27342387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:226ce9ec935d4ae0207fd3c9d44b8edd62302a528ee66c5adb39f7ac5b8a0993
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28009396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbed079020c533dbc7ca626067d743bf7effce2e4c895f104846afd8f4943a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f8e318d098424cef87513f4c834987f20c608791646c6b1a3ef60ed57408ddb6`  
		Last Modified: Thu, 26 Jan 2023 05:14:22 GMT  
		Size: 28.0 MB (28009396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230126`

```console
$ docker pull ubuntu@sha256:9a0bdde4188b896a372804be2384015e90e3f84906b750c1a53539b585fbbe7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230126` - linux; amd64

```console
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230126` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230126` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:61bd0b97000996232eb07b8d0e9375d14197f78aa850c2506417ef995a7199a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27342387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be1f66f70f66ef43503292e38ccbfc14f2d5464e7736344783a8fc7bb339a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b150fd943bcd54ef788cece17523d19031f745b099a798de65247900d102e18`  
		Last Modified: Thu, 26 Jan 2023 05:14:03 GMT  
		Size: 27.3 MB (27342387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230126` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230126` - linux; s390x

```console
$ docker pull ubuntu@sha256:226ce9ec935d4ae0207fd3c9d44b8edd62302a528ee66c5adb39f7ac5b8a0993
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28009396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbed079020c533dbc7ca626067d743bf7effce2e4c895f104846afd8f4943a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f8e318d098424cef87513f4c834987f20c608791646c6b1a3ef60ed57408ddb6`  
		Last Modified: Thu, 26 Jan 2023 05:14:22 GMT  
		Size: 28.0 MB (28009396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:a630e0fd2ea08f74080cddba4063fb9a840526697c551f52a183c674e3130179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic` - linux; amd64

```console
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dae786ed48a53dd5568147addd2a80c41f7576823e0cba466c5520003a169ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7096432b6a9855592152ad8009431b92d7aa40980c9c94684fcc72626bbbab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:05f69cab0b799028e03233ffa93abd2d0b426412cff70959a07a29a437447ee3`  
		Last Modified: Thu, 26 Jan 2023 12:14:10 GMT  
		Size: 25.8 MB (25757647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:c4b1f492c91d866555c6eb6335660e39fa7153eb4aecb19e4f4893d580d14a3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91297aceb6d3e297e45ec91916dbea079b90ae1c7edbaf14a99c41d3f493f537`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe4914a812d394969d56f220e5ddb037a62164607a937ca866bf4ee592a8799a`  
		Last Modified: Thu, 26 Jan 2023 12:14:28 GMT  
		Size: 25.5 MB (25487159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230126`

```console
$ docker pull ubuntu@sha256:a630e0fd2ea08f74080cddba4063fb9a840526697c551f52a183c674e3130179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic-20230126` - linux; amd64

```console
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230126` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230126` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dae786ed48a53dd5568147addd2a80c41f7576823e0cba466c5520003a169ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7096432b6a9855592152ad8009431b92d7aa40980c9c94684fcc72626bbbab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:05f69cab0b799028e03233ffa93abd2d0b426412cff70959a07a29a437447ee3`  
		Last Modified: Thu, 26 Jan 2023 12:14:10 GMT  
		Size: 25.8 MB (25757647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230126` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230126` - linux; s390x

```console
$ docker pull ubuntu@sha256:c4b1f492c91d866555c6eb6335660e39fa7153eb4aecb19e4f4893d580d14a3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91297aceb6d3e297e45ec91916dbea079b90ae1c7edbaf14a99c41d3f493f537`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe4914a812d394969d56f220e5ddb037a62164607a937ca866bf4ee592a8799a`  
		Last Modified: Thu, 26 Jan 2023 12:14:28 GMT  
		Size: 25.5 MB (25487159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:9a0bdde4188b896a372804be2384015e90e3f84906b750c1a53539b585fbbe7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:61bd0b97000996232eb07b8d0e9375d14197f78aa850c2506417ef995a7199a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27342387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be1f66f70f66ef43503292e38ccbfc14f2d5464e7736344783a8fc7bb339a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b150fd943bcd54ef788cece17523d19031f745b099a798de65247900d102e18`  
		Last Modified: Thu, 26 Jan 2023 05:14:03 GMT  
		Size: 27.3 MB (27342387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:226ce9ec935d4ae0207fd3c9d44b8edd62302a528ee66c5adb39f7ac5b8a0993
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28009396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbed079020c533dbc7ca626067d743bf7effce2e4c895f104846afd8f4943a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f8e318d098424cef87513f4c834987f20c608791646c6b1a3ef60ed57408ddb6`  
		Last Modified: Thu, 26 Jan 2023 05:14:22 GMT  
		Size: 28.0 MB (28009396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:678c136e4e918eff1c5e83383859e1ea2227d75ae5fe662c9122711aa6594a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0c8e3367a3fe9b703c759e1c148c5809df1a2734f8f37529bd11fbcfd34b1d1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d2fb228861107934403e776544a3f516bc7123a1275d52f1992bada8e94d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:24 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:29 GMT
ADD file:c6e9b4142d0eef696dbc592460bdbd505f41a98d02ba1c7a84caedbb5f84ea1b in / 
# Sat, 28 Jan 2023 05:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29d183ded65aecf549f39ef891c21feb9034b5b10f341533b4af297bb5c60bb8`  
		Last Modified: Sat, 28 Jan 2023 05:21:31 GMT  
		Size: 25.8 MB (25802344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:af9488f1c2d5b6b3d0052c1bba305d8d532dea8c909a67bf8e4ab80fb941eaef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25486743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a9b2f2593848f8bbbfe35751460fdc9625ad88582cd228a1b8a6ae5fd1159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:10:10 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:10:12 GMT
ADD file:b85f8b675931991dc4361ad29563c508e8cdd381491f1da64b998d7742f72c42 in / 
# Sat, 28 Jan 2023 05:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24a981375fc3c6ae016cae56fbf42f85436ada457d63c95255694c34e6f336a4`  
		Last Modified: Sat, 28 Jan 2023 05:21:50 GMT  
		Size: 25.5 MB (25486743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230128`

```console
$ docker pull ubuntu@sha256:678c136e4e918eff1c5e83383859e1ea2227d75ae5fe662c9122711aa6594a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230128` - linux; amd64

```console
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230128` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230128` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0c8e3367a3fe9b703c759e1c148c5809df1a2734f8f37529bd11fbcfd34b1d1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d2fb228861107934403e776544a3f516bc7123a1275d52f1992bada8e94d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:24 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:29 GMT
ADD file:c6e9b4142d0eef696dbc592460bdbd505f41a98d02ba1c7a84caedbb5f84ea1b in / 
# Sat, 28 Jan 2023 05:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29d183ded65aecf549f39ef891c21feb9034b5b10f341533b4af297bb5c60bb8`  
		Last Modified: Sat, 28 Jan 2023 05:21:31 GMT  
		Size: 25.8 MB (25802344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230128` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230128` - linux; s390x

```console
$ docker pull ubuntu@sha256:af9488f1c2d5b6b3d0052c1bba305d8d532dea8c909a67bf8e4ab80fb941eaef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25486743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a9b2f2593848f8bbbfe35751460fdc9625ad88582cd228a1b8a6ae5fd1159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:10:10 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:10:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:10:12 GMT
ADD file:b85f8b675931991dc4361ad29563c508e8cdd381491f1da64b998d7742f72c42 in / 
# Sat, 28 Jan 2023 05:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:24a981375fc3c6ae016cae56fbf42f85436ada457d63c95255694c34e6f336a4`  
		Last Modified: Sat, 28 Jan 2023 05:21:50 GMT  
		Size: 25.5 MB (25486743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:a630e0fd2ea08f74080cddba4063fb9a840526697c551f52a183c674e3130179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dae786ed48a53dd5568147addd2a80c41f7576823e0cba466c5520003a169ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7096432b6a9855592152ad8009431b92d7aa40980c9c94684fcc72626bbbab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:05f69cab0b799028e03233ffa93abd2d0b426412cff70959a07a29a437447ee3`  
		Last Modified: Thu, 26 Jan 2023 12:14:10 GMT  
		Size: 25.8 MB (25757647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:c4b1f492c91d866555c6eb6335660e39fa7153eb4aecb19e4f4893d580d14a3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91297aceb6d3e297e45ec91916dbea079b90ae1c7edbaf14a99c41d3f493f537`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe4914a812d394969d56f220e5ddb037a62164607a937ca866bf4ee592a8799a`  
		Last Modified: Thu, 26 Jan 2023 12:14:28 GMT  
		Size: 25.5 MB (25487159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
