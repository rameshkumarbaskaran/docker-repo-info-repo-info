<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230624`](#ubuntufocal-20230624)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230624`](#ubuntujammy-20230624)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230624`](#ubuntukinetic-20230624)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230615`](#ubuntulunar-20230615)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230624`](#ubuntumantic-20230624)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:5c2c5828d42b603726d850974597df0838e6a79fd0569249df2f710878a148c5
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
$ docker pull ubuntu@sha256:8c38f4ea0b178a98e4f9f831b29b7966d6654414c1dc008591c6ec77de3bf2c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14be0685b7682b182af5b862c9638cb1cb4ca1a70bd5aa90deed96e9cca881e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01085d60b3a624c06a7132ff0749efc6e6565d9f2531d7685ff559fb5d0f669f`  
		Last Modified: Wed, 28 Jun 2023 10:13:37 GMT  
		Size: 27.5 MB (27505622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3831296f7467818605f4c8782b1a74a3488547102640e9cb8b41c42b44e7f526
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef263d65a04f7a877f4868d790eef952ec3a69e4143477edc9f3cc80c4f9c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f6069ed163b7975b49dc9e8925a15a02473293dca6513363fb11c08764520b8`  
		Last Modified: Mon, 05 Jun 2023 17:26:46 GMT  
		Size: 23.6 MB (23611936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7bdccf116db125b3e6e39eb67ca9e2ae890386acf95a13a4e8b69466b6eba5e2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a7b6c94869fe72f4c96fd84e37eebad67cc4d521b4cfdb9434d498925a49a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd7ea62b7af53fe93cb837560acd7903ee12e26127affb518c2b9efc6500d503`  
		Last Modified: Wed, 28 Jun 2023 10:13:43 GMT  
		Size: 26.0 MB (25973322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7f8e05f0fe5051ae5758e32e10fb8f4d03dadbeaed11ad1b4568d55c7b807212
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b50995e177b3470bd0ac3d8f8ef8937314b4a3c5de95b973394b33d4e401126`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:233267f91274613e61446d456ea83cb8f9f41915ab82de44f313979f9a7464e5`  
		Last Modified: Wed, 28 Jun 2023 10:13:56 GMT  
		Size: 32.1 MB (32070528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7fa3e1a7f357f2ee21918f3ad5eeab7a0d02a7452acdaecc47f585ed6e52d76a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26350273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bdc248f7d72bc0aa775d61bceae878a8443d11d651d172a28fa56644492df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0ebf1bc80a393479c293dfa52056fa26e7e3699214a6559bd7004f7c2d3c2832`  
		Last Modified: Wed, 28 Jun 2023 10:14:02 GMT  
		Size: 26.4 MB (26350273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:dcbd90ebfbcfd693bdf862db527c4403411c830b9c60475031008b5930138c66
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:107cc410d683e41f2765125ec3b3aba514025348590539fcc079fa02d54f5708
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab733017eab481028e4f46a149cba2e422b2bc0c15a07c9bd29e7d431b568546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ccff9014dcde158442f3978d42c5311f5833a9a4200b72f93a87ca7f7542c39a`  
		Last Modified: Wed, 28 Jun 2023 08:59:07 GMT  
		Size: 28.0 MB (28016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:0cb7fa2cf2e10da0b8eb790247d0f1ea69d39a247b16d6d01d3309841745f417
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
$ docker pull ubuntu@sha256:d36481db487c935436420cc4b705db8c81eec3872085ebd27963b775695fbe24
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692eb4a905c074054e0a35d647671f0e32ed150d15b23fd7bc745cfb2fdeddbd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ad6ea492c35ef48892b4587449510d372516d5969073eeaa6601a380e861c57`  
		Last Modified: Wed, 28 Jun 2023 09:32:54 GMT  
		Size: 26.7 MB (26704806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5dc1502337b177771dd9904822cde9abd2b26ee4014a3c6df7e912a9ef103db3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25098670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120758c0ceafe38a213551ecf496a3b05011b323c13e36840d566b2ee02416d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7eb2ece7978deb374e0aa4623aa1a44d513c34c7a56e23251a0dfbba314ea260`  
		Last Modified: Mon, 05 Jun 2023 17:21:41 GMT  
		Size: 25.1 MB (25098670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:885e33391340ef6e36f410ef4382241f4faff59986ba17ce55ab9bfbc4f79efa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25772218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7a4dffcd0c03c36024e7bf725b50e96de232eaed0ee707b14baa9bbd22b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:50 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:16:58 GMT
ADD file:a41ad4058e77a6f1ee9800af03cf13403d5d844e876246ba55c4ceb2106b6d5f in / 
# Wed, 28 Jun 2023 09:16:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e61f4c584b9fdc42954629a569ca071b0df9fcec1269a44471dea738cc5b76c3`  
		Last Modified: Wed, 28 Jun 2023 09:33:01 GMT  
		Size: 25.8 MB (25772218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:749c3b9b3c562efd292d7e18cd505049be265a3a5d47eb7d13f564e8ab63883e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6309ce79ee254263bf56ae4d2130dca49695a0b6826b8a27283a940b146297f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7e018351ec7279f5a90b1b51c00c5f3b0ed9ef61d2d727237082a772ae36f3a`  
		Last Modified: Wed, 28 Jun 2023 09:33:14 GMT  
		Size: 31.1 MB (31113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:0e44a443176bc6ca4e93ac2e465db208c43934238f410f378dc3c998eee696b5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94aa2bec78551a9bd8a92d09f4fe0504cbd6f72a3ebaf9820bbcb93897b2aed1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:31:17 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:31:19 GMT
ADD file:e6e44f70accdecf50c8942a8e70c4d2c1d419d1d61696730d8aeda653da7216b in / 
# Wed, 28 Jun 2023 08:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7dfef942861c66b1cea3ce2cc82694e398544893132321d00bace936daa2c360`  
		Last Modified: Wed, 28 Jun 2023 09:33:20 GMT  
		Size: 25.5 MB (25490150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:b5d5cddaeb8d2f150660cf8f9a1203dd450ac765e6c07630176ac6486eceaddb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:6b7f8b6a5280fe23d857ac4cd887805f2a7d014d3d88dccedd81379291a54a34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25716588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed40f2186d81239c9993cac2d5749fcad7ee65da4786f87d8e3d0caea927e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:11:16 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:11:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:11:18 GMT
ADD file:3974fe053080180d99954042c25b3bd0c82e320fb4521b197cbc45f21885fc43 in / 
# Thu, 15 Jun 2023 08:11:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1611e8f17f580c929b21787327a1e5133fd1c1954ec9b270101aee4380735e40`  
		Last Modified: Thu, 15 Jun 2023 09:08:53 GMT  
		Size: 25.7 MB (25716588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:15bd920d92eea26db608c1238f7adc4b874d723d0be737e8c6fddbb73a68fae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:266cbca633bcb1356b9be281efe251782d30830cee0c0cf6a3c952a3a655f040
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26945285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3732473f881aa819c8754dc83b3bc7afc00361ea6090c135c72ccd38c9fd3637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4221febb096369c46cecc96ff4b3504b9ee19e25c6524e5da970ef0b30ee1b20`  
		Last Modified: Wed, 28 Jun 2023 09:26:34 GMT  
		Size: 26.9 MB (26945285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15ab070a0555d8274bb60513b343130b956ff0fed9288e5b7f3071c5ef434691
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26132279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bf20c5602e90cfbd38fe9170c4dd275dadd670b9eec3fe694e0672f53ab28d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837d8d26a53fc170f12f00f7943b0b3acd3a96dda6f6a60334b9ecf804d6899f`  
		Last Modified: Wed, 28 Jun 2023 09:26:43 GMT  
		Size: 26.1 MB (26132279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d261988dca9e780ecaf1ef7efcc746a2586810a686e999cf723a4f82c06d0bf7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30969695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402b62167bd7a5f530c1468e1fa8b6add4abe697dd921f85f12bba779088477`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e54d65d204131d9218cb383a0e44c321fc564d65b9a0bb4d6b4b6c749d20152f`  
		Last Modified: Wed, 28 Jun 2023 09:26:56 GMT  
		Size: 31.0 MB (30969695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:64ed81ed8782fb3323ae81aa60141d480787cd68b56fcd1a40be02b3be47d303
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8ecbb7ea7af1d7ed8af19d1e5b2614c0f5591cb25be48369e53b2122d5f76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:24:14 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:24:16 GMT
ADD file:6046e0887f51e3cd521761c62077e42ceb11c3a32d6ecd6b0b32f7d9fbb83dec in / 
# Wed, 28 Jun 2023 08:24:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da055310d6b309c0380a1d16ab6cd974a850123c5014f1e57d02df5852288ef5`  
		Last Modified: Wed, 28 Jun 2023 09:27:02 GMT  
		Size: 25.8 MB (25757906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:15bd920d92eea26db608c1238f7adc4b874d723d0be737e8c6fddbb73a68fae9
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
$ docker pull ubuntu@sha256:266cbca633bcb1356b9be281efe251782d30830cee0c0cf6a3c952a3a655f040
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26945285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3732473f881aa819c8754dc83b3bc7afc00361ea6090c135c72ccd38c9fd3637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4221febb096369c46cecc96ff4b3504b9ee19e25c6524e5da970ef0b30ee1b20`  
		Last Modified: Wed, 28 Jun 2023 09:26:34 GMT  
		Size: 26.9 MB (26945285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15ab070a0555d8274bb60513b343130b956ff0fed9288e5b7f3071c5ef434691
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26132279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bf20c5602e90cfbd38fe9170c4dd275dadd670b9eec3fe694e0672f53ab28d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837d8d26a53fc170f12f00f7943b0b3acd3a96dda6f6a60334b9ecf804d6899f`  
		Last Modified: Wed, 28 Jun 2023 09:26:43 GMT  
		Size: 26.1 MB (26132279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d261988dca9e780ecaf1ef7efcc746a2586810a686e999cf723a4f82c06d0bf7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30969695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402b62167bd7a5f530c1468e1fa8b6add4abe697dd921f85f12bba779088477`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e54d65d204131d9218cb383a0e44c321fc564d65b9a0bb4d6b4b6c749d20152f`  
		Last Modified: Wed, 28 Jun 2023 09:26:56 GMT  
		Size: 31.0 MB (30969695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:64ed81ed8782fb3323ae81aa60141d480787cd68b56fcd1a40be02b3be47d303
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8ecbb7ea7af1d7ed8af19d1e5b2614c0f5591cb25be48369e53b2122d5f76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:24:14 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:24:16 GMT
ADD file:6046e0887f51e3cd521761c62077e42ceb11c3a32d6ecd6b0b32f7d9fbb83dec in / 
# Wed, 28 Jun 2023 08:24:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da055310d6b309c0380a1d16ab6cd974a850123c5014f1e57d02df5852288ef5`  
		Last Modified: Wed, 28 Jun 2023 09:27:02 GMT  
		Size: 25.8 MB (25757906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:5c2c5828d42b603726d850974597df0838e6a79fd0569249df2f710878a148c5
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
$ docker pull ubuntu@sha256:8c38f4ea0b178a98e4f9f831b29b7966d6654414c1dc008591c6ec77de3bf2c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14be0685b7682b182af5b862c9638cb1cb4ca1a70bd5aa90deed96e9cca881e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01085d60b3a624c06a7132ff0749efc6e6565d9f2531d7685ff559fb5d0f669f`  
		Last Modified: Wed, 28 Jun 2023 10:13:37 GMT  
		Size: 27.5 MB (27505622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3831296f7467818605f4c8782b1a74a3488547102640e9cb8b41c42b44e7f526
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef263d65a04f7a877f4868d790eef952ec3a69e4143477edc9f3cc80c4f9c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f6069ed163b7975b49dc9e8925a15a02473293dca6513363fb11c08764520b8`  
		Last Modified: Mon, 05 Jun 2023 17:26:46 GMT  
		Size: 23.6 MB (23611936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7bdccf116db125b3e6e39eb67ca9e2ae890386acf95a13a4e8b69466b6eba5e2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a7b6c94869fe72f4c96fd84e37eebad67cc4d521b4cfdb9434d498925a49a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd7ea62b7af53fe93cb837560acd7903ee12e26127affb518c2b9efc6500d503`  
		Last Modified: Wed, 28 Jun 2023 10:13:43 GMT  
		Size: 26.0 MB (25973322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7f8e05f0fe5051ae5758e32e10fb8f4d03dadbeaed11ad1b4568d55c7b807212
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b50995e177b3470bd0ac3d8f8ef8937314b4a3c5de95b973394b33d4e401126`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:233267f91274613e61446d456ea83cb8f9f41915ab82de44f313979f9a7464e5`  
		Last Modified: Wed, 28 Jun 2023 10:13:56 GMT  
		Size: 32.1 MB (32070528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:7fa3e1a7f357f2ee21918f3ad5eeab7a0d02a7452acdaecc47f585ed6e52d76a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26350273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bdc248f7d72bc0aa775d61bceae878a8443d11d651d172a28fa56644492df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0ebf1bc80a393479c293dfa52056fa26e7e3699214a6559bd7004f7c2d3c2832`  
		Last Modified: Wed, 28 Jun 2023 10:14:02 GMT  
		Size: 26.4 MB (26350273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230624`

```console
$ docker pull ubuntu@sha256:79e2688b1c30870cb5241a7aff1000ba3da6220463627b6385b87964050c6d80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230624` - linux; amd64

```console
$ docker pull ubuntu@sha256:8c38f4ea0b178a98e4f9f831b29b7966d6654414c1dc008591c6ec77de3bf2c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14be0685b7682b182af5b862c9638cb1cb4ca1a70bd5aa90deed96e9cca881e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:01085d60b3a624c06a7132ff0749efc6e6565d9f2531d7685ff559fb5d0f669f`  
		Last Modified: Wed, 28 Jun 2023 10:13:37 GMT  
		Size: 27.5 MB (27505622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230624` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7bdccf116db125b3e6e39eb67ca9e2ae890386acf95a13a4e8b69466b6eba5e2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a7b6c94869fe72f4c96fd84e37eebad67cc4d521b4cfdb9434d498925a49a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd7ea62b7af53fe93cb837560acd7903ee12e26127affb518c2b9efc6500d503`  
		Last Modified: Wed, 28 Jun 2023 10:13:43 GMT  
		Size: 26.0 MB (25973322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230624` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:7f8e05f0fe5051ae5758e32e10fb8f4d03dadbeaed11ad1b4568d55c7b807212
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b50995e177b3470bd0ac3d8f8ef8937314b4a3c5de95b973394b33d4e401126`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:233267f91274613e61446d456ea83cb8f9f41915ab82de44f313979f9a7464e5`  
		Last Modified: Wed, 28 Jun 2023 10:13:56 GMT  
		Size: 32.1 MB (32070528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230624` - linux; s390x

```console
$ docker pull ubuntu@sha256:7fa3e1a7f357f2ee21918f3ad5eeab7a0d02a7452acdaecc47f585ed6e52d76a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26350273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bdc248f7d72bc0aa775d61bceae878a8443d11d651d172a28fa56644492df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0ebf1bc80a393479c293dfa52056fa26e7e3699214a6559bd7004f7c2d3c2832`  
		Last Modified: Wed, 28 Jun 2023 10:14:02 GMT  
		Size: 26.4 MB (26350273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:dcbd90ebfbcfd693bdf862db527c4403411c830b9c60475031008b5930138c66
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:107cc410d683e41f2765125ec3b3aba514025348590539fcc079fa02d54f5708
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab733017eab481028e4f46a149cba2e422b2bc0c15a07c9bd29e7d431b568546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ccff9014dcde158442f3978d42c5311f5833a9a4200b72f93a87ca7f7542c39a`  
		Last Modified: Wed, 28 Jun 2023 08:59:07 GMT  
		Size: 28.0 MB (28016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230624`

```console
$ docker pull ubuntu@sha256:4f502f4d35565009ee195ec3752e21d8220f3b70ef37b191454c1bd232bda47c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230624` - linux; amd64

```console
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230624` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230624` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230624` - linux; s390x

```console
$ docker pull ubuntu@sha256:107cc410d683e41f2765125ec3b3aba514025348590539fcc079fa02d54f5708
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab733017eab481028e4f46a149cba2e422b2bc0c15a07c9bd29e7d431b568546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ccff9014dcde158442f3978d42c5311f5833a9a4200b72f93a87ca7f7542c39a`  
		Last Modified: Wed, 28 Jun 2023 08:59:07 GMT  
		Size: 28.0 MB (28016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:0cb7fa2cf2e10da0b8eb790247d0f1ea69d39a247b16d6d01d3309841745f417
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
$ docker pull ubuntu@sha256:d36481db487c935436420cc4b705db8c81eec3872085ebd27963b775695fbe24
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692eb4a905c074054e0a35d647671f0e32ed150d15b23fd7bc745cfb2fdeddbd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ad6ea492c35ef48892b4587449510d372516d5969073eeaa6601a380e861c57`  
		Last Modified: Wed, 28 Jun 2023 09:32:54 GMT  
		Size: 26.7 MB (26704806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5dc1502337b177771dd9904822cde9abd2b26ee4014a3c6df7e912a9ef103db3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25098670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120758c0ceafe38a213551ecf496a3b05011b323c13e36840d566b2ee02416d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7eb2ece7978deb374e0aa4623aa1a44d513c34c7a56e23251a0dfbba314ea260`  
		Last Modified: Mon, 05 Jun 2023 17:21:41 GMT  
		Size: 25.1 MB (25098670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:885e33391340ef6e36f410ef4382241f4faff59986ba17ce55ab9bfbc4f79efa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25772218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7a4dffcd0c03c36024e7bf725b50e96de232eaed0ee707b14baa9bbd22b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:50 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:16:58 GMT
ADD file:a41ad4058e77a6f1ee9800af03cf13403d5d844e876246ba55c4ceb2106b6d5f in / 
# Wed, 28 Jun 2023 09:16:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e61f4c584b9fdc42954629a569ca071b0df9fcec1269a44471dea738cc5b76c3`  
		Last Modified: Wed, 28 Jun 2023 09:33:01 GMT  
		Size: 25.8 MB (25772218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:749c3b9b3c562efd292d7e18cd505049be265a3a5d47eb7d13f564e8ab63883e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6309ce79ee254263bf56ae4d2130dca49695a0b6826b8a27283a940b146297f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7e018351ec7279f5a90b1b51c00c5f3b0ed9ef61d2d727237082a772ae36f3a`  
		Last Modified: Wed, 28 Jun 2023 09:33:14 GMT  
		Size: 31.1 MB (31113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:0e44a443176bc6ca4e93ac2e465db208c43934238f410f378dc3c998eee696b5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94aa2bec78551a9bd8a92d09f4fe0504cbd6f72a3ebaf9820bbcb93897b2aed1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:31:17 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:31:19 GMT
ADD file:e6e44f70accdecf50c8942a8e70c4d2c1d419d1d61696730d8aeda653da7216b in / 
# Wed, 28 Jun 2023 08:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7dfef942861c66b1cea3ce2cc82694e398544893132321d00bace936daa2c360`  
		Last Modified: Wed, 28 Jun 2023 09:33:20 GMT  
		Size: 25.5 MB (25490150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230624`

```console
$ docker pull ubuntu@sha256:531268611d8640bb659c782a77f5214928900da779f589098ec4e0582faad8c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic-20230624` - linux; amd64

```console
$ docker pull ubuntu@sha256:d36481db487c935436420cc4b705db8c81eec3872085ebd27963b775695fbe24
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692eb4a905c074054e0a35d647671f0e32ed150d15b23fd7bc745cfb2fdeddbd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ad6ea492c35ef48892b4587449510d372516d5969073eeaa6601a380e861c57`  
		Last Modified: Wed, 28 Jun 2023 09:32:54 GMT  
		Size: 26.7 MB (26704806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230624` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:885e33391340ef6e36f410ef4382241f4faff59986ba17ce55ab9bfbc4f79efa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25772218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7a4dffcd0c03c36024e7bf725b50e96de232eaed0ee707b14baa9bbd22b98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:50 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:16:58 GMT
ADD file:a41ad4058e77a6f1ee9800af03cf13403d5d844e876246ba55c4ceb2106b6d5f in / 
# Wed, 28 Jun 2023 09:16:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e61f4c584b9fdc42954629a569ca071b0df9fcec1269a44471dea738cc5b76c3`  
		Last Modified: Wed, 28 Jun 2023 09:33:01 GMT  
		Size: 25.8 MB (25772218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230624` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:749c3b9b3c562efd292d7e18cd505049be265a3a5d47eb7d13f564e8ab63883e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6309ce79ee254263bf56ae4d2130dca49695a0b6826b8a27283a940b146297f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7e018351ec7279f5a90b1b51c00c5f3b0ed9ef61d2d727237082a772ae36f3a`  
		Last Modified: Wed, 28 Jun 2023 09:33:14 GMT  
		Size: 31.1 MB (31113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230624` - linux; s390x

```console
$ docker pull ubuntu@sha256:0e44a443176bc6ca4e93ac2e465db208c43934238f410f378dc3c998eee696b5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25490150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94aa2bec78551a9bd8a92d09f4fe0504cbd6f72a3ebaf9820bbcb93897b2aed1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:31:17 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:31:17 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:31:19 GMT
ADD file:e6e44f70accdecf50c8942a8e70c4d2c1d419d1d61696730d8aeda653da7216b in / 
# Wed, 28 Jun 2023 08:31:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7dfef942861c66b1cea3ce2cc82694e398544893132321d00bace936daa2c360`  
		Last Modified: Wed, 28 Jun 2023 09:33:20 GMT  
		Size: 25.5 MB (25490150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:dcbd90ebfbcfd693bdf862db527c4403411c830b9c60475031008b5930138c66
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:107cc410d683e41f2765125ec3b3aba514025348590539fcc079fa02d54f5708
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab733017eab481028e4f46a149cba2e422b2bc0c15a07c9bd29e7d431b568546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ccff9014dcde158442f3978d42c5311f5833a9a4200b72f93a87ca7f7542c39a`  
		Last Modified: Wed, 28 Jun 2023 08:59:07 GMT  
		Size: 28.0 MB (28016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:b5d5cddaeb8d2f150660cf8f9a1203dd450ac765e6c07630176ac6486eceaddb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:6b7f8b6a5280fe23d857ac4cd887805f2a7d014d3d88dccedd81379291a54a34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25716588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed40f2186d81239c9993cac2d5749fcad7ee65da4786f87d8e3d0caea927e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:11:16 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:11:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:11:18 GMT
ADD file:3974fe053080180d99954042c25b3bd0c82e320fb4521b197cbc45f21885fc43 in / 
# Thu, 15 Jun 2023 08:11:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1611e8f17f580c929b21787327a1e5133fd1c1954ec9b270101aee4380735e40`  
		Last Modified: Thu, 15 Jun 2023 09:08:53 GMT  
		Size: 25.7 MB (25716588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230615`

```console
$ docker pull ubuntu@sha256:b5d5cddaeb8d2f150660cf8f9a1203dd450ac765e6c07630176ac6486eceaddb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230615` - linux; amd64

```console
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; s390x

```console
$ docker pull ubuntu@sha256:6b7f8b6a5280fe23d857ac4cd887805f2a7d014d3d88dccedd81379291a54a34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25716588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed40f2186d81239c9993cac2d5749fcad7ee65da4786f87d8e3d0caea927e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:11:16 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:11:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:11:18 GMT
ADD file:3974fe053080180d99954042c25b3bd0c82e320fb4521b197cbc45f21885fc43 in / 
# Thu, 15 Jun 2023 08:11:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1611e8f17f580c929b21787327a1e5133fd1c1954ec9b270101aee4380735e40`  
		Last Modified: Thu, 15 Jun 2023 09:08:53 GMT  
		Size: 25.7 MB (25716588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:15bd920d92eea26db608c1238f7adc4b874d723d0be737e8c6fddbb73a68fae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:266cbca633bcb1356b9be281efe251782d30830cee0c0cf6a3c952a3a655f040
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26945285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3732473f881aa819c8754dc83b3bc7afc00361ea6090c135c72ccd38c9fd3637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4221febb096369c46cecc96ff4b3504b9ee19e25c6524e5da970ef0b30ee1b20`  
		Last Modified: Wed, 28 Jun 2023 09:26:34 GMT  
		Size: 26.9 MB (26945285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15ab070a0555d8274bb60513b343130b956ff0fed9288e5b7f3071c5ef434691
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26132279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bf20c5602e90cfbd38fe9170c4dd275dadd670b9eec3fe694e0672f53ab28d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837d8d26a53fc170f12f00f7943b0b3acd3a96dda6f6a60334b9ecf804d6899f`  
		Last Modified: Wed, 28 Jun 2023 09:26:43 GMT  
		Size: 26.1 MB (26132279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d261988dca9e780ecaf1ef7efcc746a2586810a686e999cf723a4f82c06d0bf7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30969695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402b62167bd7a5f530c1468e1fa8b6add4abe697dd921f85f12bba779088477`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e54d65d204131d9218cb383a0e44c321fc564d65b9a0bb4d6b4b6c749d20152f`  
		Last Modified: Wed, 28 Jun 2023 09:26:56 GMT  
		Size: 31.0 MB (30969695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:64ed81ed8782fb3323ae81aa60141d480787cd68b56fcd1a40be02b3be47d303
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8ecbb7ea7af1d7ed8af19d1e5b2614c0f5591cb25be48369e53b2122d5f76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:24:14 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:24:16 GMT
ADD file:6046e0887f51e3cd521761c62077e42ceb11c3a32d6ecd6b0b32f7d9fbb83dec in / 
# Wed, 28 Jun 2023 08:24:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da055310d6b309c0380a1d16ab6cd974a850123c5014f1e57d02df5852288ef5`  
		Last Modified: Wed, 28 Jun 2023 09:27:02 GMT  
		Size: 25.8 MB (25757906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20230624`

```console
$ docker pull ubuntu@sha256:5a2170c50f92e6cd9ba056d61c347a5c272bff5935293b98aab7582aa1a55b99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20230624` - linux; amd64

```console
$ docker pull ubuntu@sha256:266cbca633bcb1356b9be281efe251782d30830cee0c0cf6a3c952a3a655f040
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26945285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3732473f881aa819c8754dc83b3bc7afc00361ea6090c135c72ccd38c9fd3637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:22 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:22 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:23:24 GMT
ADD file:ce14b5aa15734922ec61b739c654f0d2843757c5f260778d4ecd9aa097cfacaf in / 
# Wed, 28 Jun 2023 08:23:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4221febb096369c46cecc96ff4b3504b9ee19e25c6524e5da970ef0b30ee1b20`  
		Last Modified: Wed, 28 Jun 2023 09:26:34 GMT  
		Size: 26.9 MB (26945285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230624` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:15ab070a0555d8274bb60513b343130b956ff0fed9288e5b7f3071c5ef434691
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26132279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bf20c5602e90cfbd38fe9170c4dd275dadd670b9eec3fe694e0672f53ab28d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:48:57 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:48:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:48:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:48:58 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:49:02 GMT
ADD file:40c27ea75a8cc64630db8f6d3d5c770eaa2fd339a996f54bab5f7e912d333d68 in / 
# Wed, 28 Jun 2023 08:49:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837d8d26a53fc170f12f00f7943b0b3acd3a96dda6f6a60334b9ecf804d6899f`  
		Last Modified: Wed, 28 Jun 2023 09:26:43 GMT  
		Size: 26.1 MB (26132279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230624` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d261988dca9e780ecaf1ef7efcc746a2586810a686e999cf723a4f82c06d0bf7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30969695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402b62167bd7a5f530c1468e1fa8b6add4abe697dd921f85f12bba779088477`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:52:24 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:52:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:52:24 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:52:27 GMT
ADD file:3190365fa0ba0de5c8c20d6508d6324ccc027f301a3647080c04c6ae4296b232 in / 
# Wed, 28 Jun 2023 08:52:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e54d65d204131d9218cb383a0e44c321fc564d65b9a0bb4d6b4b6c749d20152f`  
		Last Modified: Wed, 28 Jun 2023 09:26:56 GMT  
		Size: 31.0 MB (30969695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230624` - linux; s390x

```console
$ docker pull ubuntu@sha256:64ed81ed8782fb3323ae81aa60141d480787cd68b56fcd1a40be02b3be47d303
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8ecbb7ea7af1d7ed8af19d1e5b2614c0f5591cb25be48369e53b2122d5f76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:24:14 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:24:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 08:24:16 GMT
ADD file:6046e0887f51e3cd521761c62077e42ceb11c3a32d6ecd6b0b32f7d9fbb83dec in / 
# Wed, 28 Jun 2023 08:24:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da055310d6b309c0380a1d16ab6cd974a850123c5014f1e57d02df5852288ef5`  
		Last Modified: Wed, 28 Jun 2023 09:27:02 GMT  
		Size: 25.8 MB (25757906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:b5d5cddaeb8d2f150660cf8f9a1203dd450ac765e6c07630176ac6486eceaddb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:6b7f8b6a5280fe23d857ac4cd887805f2a7d014d3d88dccedd81379291a54a34
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25716588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed40f2186d81239c9993cac2d5749fcad7ee65da4786f87d8e3d0caea927e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:11:16 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:11:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:11:16 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:11:18 GMT
ADD file:3974fe053080180d99954042c25b3bd0c82e320fb4521b197cbc45f21885fc43 in / 
# Thu, 15 Jun 2023 08:11:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1611e8f17f580c929b21787327a1e5133fd1c1954ec9b270101aee4380735e40`  
		Last Modified: Thu, 15 Jun 2023 09:08:53 GMT  
		Size: 25.7 MB (25716588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
