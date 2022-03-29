## `debian:stable-backports`

```console
$ docker pull debian@sha256:6480649f941b58d9dc953de399b622aafe6c90cb2c6255a471113c5fa22c7db2
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
$ docker pull debian@sha256:cd2970260d96bff46222eb6298bc5bf67c06e1c0f99a5e6fed0f729c58d184de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54937910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f2718a9a61334bb82013ff4143fd1950f76e4b53366e64371721c1592492e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:23:44 GMT
ADD file:f7da55bb350a7124a320e3b75efceb266942ce3dcfb8714c591e7c44edf38bb1 in / 
# Tue, 29 Mar 2022 00:23:45 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:23:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e8a3bebe4c9af1dc419c7efc54956571acb4d17ad0924b60150c8e2aaacf40a`  
		Last Modified: Tue, 29 Mar 2022 00:30:02 GMT  
		Size: 54.9 MB (54937688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522b53bc8a7d460c83d409bbecf0e23251d937e06dcef98c236823045cfa7fd3`  
		Last Modified: Tue, 29 Mar 2022 00:30:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8e5d8f5aab43beaa1f2a2dccd7918da179f8035d75b6b3d8a94b48aeabd9ac3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7845caecc0b38370a1e314f6477997e93579d93c56527d2e6a7c19f443e17446`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:54:36 GMT
ADD file:abd8aaf2c6d51d5c52c113d618cac82fa11a158ee861ae829b97d1250d0094f1 in / 
# Tue, 29 Mar 2022 00:54:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:54:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f14611b540abb650e196e4ec7510ac9ff0b5355627c1ee4ec6756cfe2fc59c7`  
		Last Modified: Tue, 29 Mar 2022 01:10:56 GMT  
		Size: 52.5 MB (52475840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f270a7d4cc6fc1c73aefd06c8ca8fb319fee0c27db0ce11b3b92027def3fd3d`  
		Last Modified: Tue, 29 Mar 2022 01:11:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ffc2bfede771f82347cd7ca6488a16b03659de70188eccee7e9f9d45eea79695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50122540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c72d59eab1b861130bcae4979d5f7d4c7871767e859856f2d77be5823dd9a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:35:24 GMT
ADD file:f628ad367a67a919d1385cf48311ebb0883d86274244b887945cba4c453f4b35 in / 
# Thu, 17 Mar 2022 09:35:26 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:35:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a7cb48db87768c0e7194b1e29a5e16b2ab6203dcafa7213fac705c99542e5059`  
		Last Modified: Thu, 17 Mar 2022 09:51:52 GMT  
		Size: 50.1 MB (50122316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc279f0603b60ad84ac9bf56bb551e81e99990f042f8c1032f51df45fb335fd`  
		Last Modified: Thu, 17 Mar 2022 09:52:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4f134dfd7a54cbf6c79810bb67da2310106301abc95c79ae89c7fed1378af1ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53633919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c082c991dcdeca8c3fdf64b0850a9215260dcd1d5d77e0dd3312f9108b8f59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:58 GMT
ADD file:108b85901446afd3b83e29a5f9d1cbe41d8d8865f40f7fd3ba45549398494b3c in / 
# Tue, 29 Mar 2022 00:44:59 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:45:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c52bd4023d6a14e3706307f8a0f04e3da706b3785d67585cb1d5775c1f349d05`  
		Last Modified: Tue, 29 Mar 2022 00:53:13 GMT  
		Size: 53.6 MB (53633699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cd09a7a0874b234babbdc060462c88f6157946e63070288038dea499c01f98`  
		Last Modified: Tue, 29 Mar 2022 00:53:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:34ed146997c107da028402e430eb825495304e0eb83bca9808fc9dd55f87371a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55940857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ed4a7d440ebf900accdcdeca00e9ce3b089497c09491ce563e6e450db95d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:45 GMT
ADD file:79f3d24ec2b208547d39927a0d3e973fd4d1bdb5926511538937943162e48c18 in / 
# Tue, 29 Mar 2022 00:43:46 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:43:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:288ae49939b3ef190048eb92d2e9d77f91b51f9527a30d3df39de493fb27083b`  
		Last Modified: Tue, 29 Mar 2022 00:52:25 GMT  
		Size: 55.9 MB (55940633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41132ee77a302b1cd51712b81b38a91107490d75b96441fecc1ffb25087f7126`  
		Last Modified: Tue, 29 Mar 2022 00:52:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:bd007727567e32513b423f75259c65281adbb7e2cd07dc64d090235d61e9de56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53187689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba64a088d5fe1f1da1fe52309d357491abd53f18bd6307cbb2db85e98a87e81`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:56:44 GMT
ADD file:c692fb767ac3c1d9c4baa0fc6e15af57c52c5367065e85293e9ac926e8a40e76 in / 
# Thu, 17 Mar 2022 08:56:49 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:57:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:96ea1c4e2dcde973aef8bb20a482040038f9e50f6ca25a40f337065196217754`  
		Last Modified: Thu, 17 Mar 2022 10:47:47 GMT  
		Size: 53.2 MB (53187465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec4479097720cc88d4d0e74d627c29ca560c4256a9de982a9645ded35c2ca6`  
		Last Modified: Thu, 17 Mar 2022 10:47:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:02ca5404c1cb90e5f9b84c5a202ecb44b9e8912a78b0b2130363b4051f385f16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58835153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dc20fd47942b38238b1805a56487c21a5ab441f1a3bdc2e3225a94c21ea436`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:49 GMT
ADD file:9c5677819d8db26be48d5a239294edffce512138718e8e00b86d19046a2a3e49 in / 
# Tue, 29 Mar 2022 00:24:53 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:25:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3c64acf2aaabe9cf36d9fa51d66be21a1c381ca1dc4f15ab569a6794b655bb83`  
		Last Modified: Tue, 29 Mar 2022 00:38:37 GMT  
		Size: 58.8 MB (58834929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa75a73b6b790a733dd47ef58a664b685fbbc2ee0f38eb2cae2907a354462afb`  
		Last Modified: Tue, 29 Mar 2022 00:38:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:94265c31f7ee6c66e8103d7a12ea39b8fa07718341345d34b5366dabf55f23fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53210356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e324595a3c0e72f8865102f07aed330dd1f7e367c3277340dfd8c1d804239b19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:28 GMT
ADD file:9c8109e8edaf499eeaac7353760c4169d5b14f48c6cacf6000ec0bac50662266 in / 
# Tue, 29 Mar 2022 00:53:31 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:53:38 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08559879f8bc797024b3fd393eeac6e78025b622e187a7d30c39f9c6230a3cf4`  
		Last Modified: Tue, 29 Mar 2022 01:20:43 GMT  
		Size: 53.2 MB (53210134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0866d3cada0a38f97408f15f997304672ab3b3677f1e9a07433cfdcf9b1a090`  
		Last Modified: Tue, 29 Mar 2022 01:21:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
