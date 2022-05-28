## `debian:stable-backports`

```console
$ docker pull debian@sha256:8aebc075d2b7e32617ef695ce42f7c448c97847f0e49d58cc60058c38cbc8d95
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bae194a553cae1cb73a1d4ac680fdb63e360b7a288db5be0b5f157c293fcecda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54945778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3544b631dcda6bce8404755c80aa6f2c0727b93e815eb35d5b2b2cda2b3f7064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:21:45 GMT
ADD file:792adfcd9c92e3b60bc165757c7fc68b39ec3bdf9030bb209223ef47bd58da26 in / 
# Wed, 11 May 2022 01:21:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:21:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13597bb7b8ec279069b63a470ac94c1f9ddd23d20c163e6dc69a4227021bdf5d`  
		Last Modified: Wed, 11 May 2022 01:27:59 GMT  
		Size: 54.9 MB (54945555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cb1c94f64374f83d540e7ec4842e6ef46498a666378ba0534a4aefd26c3b49`  
		Last Modified: Wed, 11 May 2022 01:28:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bb6e07ace4b854ef21fe99b99107b86fc8d4672a417d2b747c3b0496671d96ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bc40eaa148c61220fa693426bd79f2e10d6e6646554aa9b2effeba47ab2835`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:54:37 GMT
ADD file:6b5d9fb1dcd89975c59319d94c9048759069ec5b363c5f03ab1207358133e06b in / 
# Wed, 11 May 2022 00:54:38 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:54:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2a4feda66e274d3031e4219d93b4c906d0c3a62930ec9636a138434eadeb8c8`  
		Last Modified: Wed, 11 May 2022 01:11:48 GMT  
		Size: 52.5 MB (52476631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d32fc2ee030caf4a5f36e17cd61c5b09d3c56d9536ae51b5fcdb5ff6e8fcec8`  
		Last Modified: Wed, 11 May 2022 01:11:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5d10878e3c7a767859f674b909bdf42f13aecc2938e9f1514d1bf7cda838895e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8fa16616ef2814bdfd98b6ef7ae3bb54b09155dd4847470f115eeb9775dfe8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:53:32 GMT
ADD file:9d8fb9bab1ab3e74c052a073c85a8ca3c807d829804ade5ad68a021ddbe2bb35 in / 
# Wed, 11 May 2022 01:53:33 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:53:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d27c72babaa762ec587d1f7cc1d0b63f7180dc5834d316959307c8d4ee3f4fcb`  
		Last Modified: Wed, 11 May 2022 02:10:07 GMT  
		Size: 50.1 MB (50134123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03736200ce161f35707fd031e9f9b1ac93c40146eb6c5239e294b56eeeca4fef`  
		Last Modified: Wed, 11 May 2022 02:10:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:716b2bb6b120704dffba15df825e7db42ba4f2852be5bf65f45bde65b09646a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53697199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6fc3561914206da3df980eaa4da006f6dbeb1954304f6595d7b887bf4aa83d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:21 GMT
ADD file:ff1cc52bba4a6a12b43ef4e8dc200d5179b265981e08a3b7a4bd2896ff2a7ff8 in / 
# Sat, 28 May 2022 00:42:22 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1e2623ac7c4f668298956a826900c9848f8de14a932c41e28bebeb1946741d06`  
		Last Modified: Sat, 28 May 2022 00:50:41 GMT  
		Size: 53.7 MB (53696974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093539695cf6715d7056998ab5d4998d8ae0e2d00368297c24d19896d4077849`  
		Last Modified: Sat, 28 May 2022 00:50:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:47e974cda1beacb1740674d787c00fa3eced7e37bf18634e97031c7b7a65e8b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56008310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31609093e76e3fbf74112fc4db72c28d2160d3befc09f595f13964f0545e11ca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:24 GMT
ADD file:d7f6d5496b54319f0d60f5cdf12d34094f5d33f49f174d4a9f1a7a6509c8057e in / 
# Sat, 28 May 2022 00:41:25 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:41:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a3312bca7d30f7a52702aa72d2757cae357a6ee0867338b83f5c368d22451f9d`  
		Last Modified: Sat, 28 May 2022 00:49:50 GMT  
		Size: 56.0 MB (56008089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2e6393c27675df6b06ab3294d8e2318d894c693962012c073112cfd1608291`  
		Last Modified: Sat, 28 May 2022 00:50:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:421c874ec0d34779ab604a322193480d38e09e8d41346a74ad7021ec5d5474d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53205812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462a98faf3d089a2177a97257b4475a527dd41f809971f7e6a8c0f7702a879f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:27:19 GMT
ADD file:346e47649524e8cc64cd2d66a9a0722a5fa4b93fbdd46ee0fa1c40cd9968ef48 in / 
# Wed, 11 May 2022 02:27:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:27:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:19ef497ced211482685ee90f3e3c6ce0906e1e37bffe14d2ee81c59123d8e6c4`  
		Last Modified: Wed, 11 May 2022 02:38:07 GMT  
		Size: 53.2 MB (53205588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18fa139109b22d5db4642378c4c02e5bcb6e35e642b2627c4bf5731d9f1aff`  
		Last Modified: Wed, 11 May 2022 02:38:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:99458e78806450e72ef3cf391bf03552b8fa70ddd1ba7be3adfb90fd94d0651f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58836755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be70d56c53a97078d340e3fcf575d90e1d4c7ab187d8440b14a27805289cb01d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:35:52 GMT
ADD file:b658d35f984b3aa5dafb205278f71f0242adfc4a4b45be026be1ff5f2cee9024 in / 
# Wed, 11 May 2022 01:36:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:36:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:11ceddd3abc1135a3dd78436a18ae61228d846481c55f210bbe8b2b6b0c413df`  
		Last Modified: Wed, 11 May 2022 01:46:07 GMT  
		Size: 58.8 MB (58836531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7494cc809b0aff1ab252544ce5be12ee8e08a8f4cb9ab74394b73ecca7710680`  
		Last Modified: Wed, 11 May 2022 01:46:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:546177261b5faaca0d75cde8cd0b7a6a257605088cc3ce8683decb9ace9c10c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53276848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe9370b3eed5fc9f0dbec0216eadcd09a6bd5aa0b4759f846066355a1809087`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:45:06 GMT
ADD file:96522e5ce7a50d833ad67450e3de3d32e9ee12642f0de49a94571afa59294408 in / 
# Sat, 28 May 2022 00:45:10 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:45:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:886de4048c228418dcc85f81c6f97297fe69c74bca502dba5f7fecdacb9f1ec2`  
		Last Modified: Sat, 28 May 2022 00:51:24 GMT  
		Size: 53.3 MB (53276626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0e6e1ebf1fe25c13ccf2b3ed7ef852445c6c9fd0622d4d620b720d7507ba43`  
		Last Modified: Sat, 28 May 2022 00:51:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
