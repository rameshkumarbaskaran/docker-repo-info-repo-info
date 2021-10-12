## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:5243ab1b76abe44ea045ad1eeee47de96619c5d6bda5c20e2395875204a904ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6380533dd62ebe2bd320f8d6d1a5b6ebd6e3ea59003cb3d9dcf609098c048518
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50436958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8474337d037b33e18c195f959ced8c9164cceb76de317883f16d2cb7c2a0484`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:36 GMT
ADD file:1254fe58a557c9bd7a44702af996bc01a041007fa31c4bfd0674a7437f83e226 in / 
# Tue, 12 Oct 2021 01:21:36 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:21:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:486fdf79d93406106977e297ffa5f755ab39b223d63b7cf84a14c0ff8f62a9d2`  
		Last Modified: Tue, 12 Oct 2021 01:27:45 GMT  
		Size: 50.4 MB (50436730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904fffecb87b762376a2a541a5fe15d370f8f82caf2241e80794a1985da62648`  
		Last Modified: Tue, 12 Oct 2021 01:27:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:00d3089bc834c350def7f1141872cba227cbf981446fda9c80ab418654d4fad8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50056f0f79d54a29ab196b609f9ec149aa40b53af5f0308efc9bad6814cb0056`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:52:56 GMT
ADD file:a042a1b4d39d508b4725145149caf6615d44e43427b4566e3839840e9dec939e in / 
# Tue, 12 Oct 2021 00:52:57 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:53:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e187af41423780e5cc95f89de4b56a3c18a2c5636f1919be23b07449d54381a7`  
		Last Modified: Tue, 12 Oct 2021 01:09:44 GMT  
		Size: 48.2 MB (48154060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fee3bcfa3710a132764abc7d51d4e4a2f8b1a1cb26b123dc2e5ec2b6a007ec`  
		Last Modified: Tue, 12 Oct 2021 01:09:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:acfe7fd2c4dc3e75c14f2e25d8f34bcb2f1f48ed1bbe34964ea092e4c915c404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e3a0f95c2d2375a2a560ca0187eb7bbd573745444a1238cd8565f84992068`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:31:12 GMT
ADD file:075763af19fd2f62d5199e9f9ece478e2602aee33c939ccd258f599d88469046 in / 
# Tue, 12 Oct 2021 01:31:13 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:31:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1e8a087bec2ff439032f91ace1191030ed684bf5807987913cb1d995565a032`  
		Last Modified: Tue, 12 Oct 2021 01:47:54 GMT  
		Size: 45.9 MB (45917917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d5fe54b7d2e0e4000dc91ff9e082e5b3328cfc66c7ea9cd92e2617e34e20cf`  
		Last Modified: Tue, 12 Oct 2021 01:48:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6d751ef6432e842e731d2eacfe3df4e190ef7aee2314d4d665d40e310cfcbd76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49222943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc392951da1a1868cdc111888754a7b4d02fa92ab7e6bdc02fcfd91c78e92fe7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:42:14 GMT
ADD file:10280ad72673a7baf3b2455f9bc16ba1c50a1d0c5a8276d89e2a786b1c84af75 in / 
# Tue, 12 Oct 2021 01:42:14 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d37bb723b5cb5b3b65952b63d77d16450a085709a53d71e1e3251bd609ea570`  
		Last Modified: Tue, 12 Oct 2021 01:50:11 GMT  
		Size: 49.2 MB (49222718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c2e0e1287f388532f7ccba9ef48bd1c75351aec0b98c30c58c88f5ed97c31`  
		Last Modified: Tue, 12 Oct 2021 01:50:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4926935f134d09402c704ac5fc6228f498df692a4f98ea8ae3e51ed97d21f0b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2e641a4b5992ed8ddd701cdc020c30d81df3e6f6ee22e3d7538efbb45d0f66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:40:58 GMT
ADD file:53dbb1fd8cfb15946c2df51556975d015470c45ae4ca8033fba41c5f31356d52 in / 
# Tue, 12 Oct 2021 01:40:58 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:41:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f657a8783f7ec563f233d088f92dcd9bf9e3a39b1d449cb9fab27caed5aadb0`  
		Last Modified: Tue, 12 Oct 2021 01:49:47 GMT  
		Size: 51.2 MB (51207558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d7f2e4b4fd74448d3c1e508cbb2de52ff827c88fed34c9cf7062ce5c0a4608`  
		Last Modified: Tue, 12 Oct 2021 01:49:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f1f3a35fda76f13e289b4ce5fe0420f350827d934981c41f49d5a6e35e7b7b23
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc6fb2b12468354066f6b9986e914740f594a46b96ef90f0ba58e96c2c8bb82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:12:34 GMT
ADD file:e8a4c8f46e0308d588aabdfa8cef54cbc9e873569fc4f06b1fb6942cb106c5b0 in / 
# Tue, 12 Oct 2021 01:12:35 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:12:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:771cec173f62208002de95d47a62059a81d70a4b0c86620fcc0f9dd6ff5deee2`  
		Last Modified: Tue, 12 Oct 2021 01:22:21 GMT  
		Size: 49.1 MB (49079493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce9ca9d67188dd30df52aeac7c4928bff77b2efa948044fa744c0fc9e0d95d`  
		Last Modified: Tue, 12 Oct 2021 01:22:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2efa26897472def3e7607da3f947623eec0ec3ba6b9ad3a43b82eaa0da4eb843
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bafe1bf448cf088e395bce39fe004c0a47834712f17bb8a2d85fec632f88ecd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:07 GMT
ADD file:1685b474962ea6fe3945c29bc49da37313319ebb22343899681a2e98b188f7a7 in / 
# Tue, 12 Oct 2021 01:27:12 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:27:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f80c6b99f8408b2bde68df0b7885d92c0fcd5531033f895599a7d09df37fe5e2`  
		Last Modified: Tue, 12 Oct 2021 01:39:27 GMT  
		Size: 54.2 MB (54183530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eb798c822c60d4194a983e9230877e5580353d3271e1a99c12cb4c64f47e60`  
		Last Modified: Tue, 12 Oct 2021 01:39:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:f6596f7eace5f84a0ccf8ecc9aac007375cb65abff75de1ba93dfdcfc5c915a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3515baf08a2e599eca5bb5135a95d75dd3812ac8ba139def5fae0f6f312b275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:43:08 GMT
ADD file:131966fcf68790a9e9a3c79c1be0f33ee52522f57e0d286fee2f2441daba4718 in / 
# Tue, 12 Oct 2021 00:43:10 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:43:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e95a5b27ccd32e7e7d080f127e6d02afb66719bec59086cf85da5f76bf785fdf`  
		Last Modified: Tue, 12 Oct 2021 00:48:58 GMT  
		Size: 49.0 MB (49004893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a3b7df1003352420c9b201bfb5ac124c79af942a562b5e916337ce44ee0e4d`  
		Last Modified: Tue, 12 Oct 2021 00:49:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
