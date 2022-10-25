## `debian:experimental`

```console
$ docker pull debian@sha256:786de0efad7f5028688b933169136b98e431bef66e654b753592683451e8b5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:154fc729cc812cedeeca8446d15d9e344067e351aacf4856156c218bf0e835a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50641427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061216c4987060efde1cba818de03f256d65af769f5e0c726c47e3cee89519d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:45:38 GMT
ADD file:1547e086dc40d3418e8f146e3b7fe2141ad7659675f0a810d3723f618ce685f3 in / 
# Tue, 25 Oct 2022 01:45:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:45:50 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:37185fef75d9c859c0943d1efbb25a8ccb6052762fdece7628188b1dd148c6b2`  
		Last Modified: Tue, 25 Oct 2022 01:51:27 GMT  
		Size: 50.6 MB (50641207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a9a9e5cbb08d19f59ebb1026adfa6311b7d5962ee3eb8789bf89adea76029`  
		Last Modified: Tue, 25 Oct 2022 01:51:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:87310c1db4556de02d9a336435fa8acc97c3d314052a6fca03412b1e33ab6ec1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49579113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e560102aeb64231d75604b0c8e462213350d04ecbd9f2e3f4f51461554431ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:08:13 GMT
ADD file:77cda19d5e418441e9326d24d111b891ea6fef72ef022d41f3ce8ba647b767ba in / 
# Tue, 25 Oct 2022 03:08:15 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:08:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ad9befb0b50f19e57ce1901a6674614f204b1b9fe169308dfec65d741d6afe7a`  
		Last Modified: Tue, 25 Oct 2022 03:14:37 GMT  
		Size: 49.6 MB (49578890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60151311cdd6a2b4d123707c3187944e77abfe29b01d668051d50e6babac1e50`  
		Last Modified: Tue, 25 Oct 2022 03:15:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:98e575e680f25762334d50f86358898f14a88a28113f784a5cb1c84db3f8aaba
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47411790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674603cfed43e0a121d076a36328e1b0e913983ac715373e9e7a7d89e0156d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:16:53 GMT
ADD file:c8c86dd8bcaccc6f60e985551be5ca8fac33d08aacb4795b6a7cb8f47a0608d3 in / 
# Tue, 25 Oct 2022 03:16:54 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:17:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d484fb83cf6edf5d285cd720b979db3135d544da4ecaea668beed729cd1ddf65`  
		Last Modified: Tue, 25 Oct 2022 03:25:29 GMT  
		Size: 47.4 MB (47411568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6d60b3efe8a4d25cdaccd3c899e16f08aea22bf0a6068dc4a16850e5ba22b0`  
		Last Modified: Tue, 25 Oct 2022 03:25:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b10e1743cef0ebd082d94f2a170ede7bb904da7863fe6626d89b28157bbef324
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52700212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c589062a6fb00ab07e5a97777d479d85ceb85f2ca05658727be9b4e9f35e613b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:47:00 GMT
ADD file:648747f4f152d5475b91db660f39083bee7a08b6556e3f2a5b75617fd9bc4614 in / 
# Tue, 04 Oct 2022 23:47:01 GMT
CMD ["bash"]
# Tue, 04 Oct 2022 23:47:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3703d828bb0519d47d75a6f11cd98cbe96f1f12dad3960f016161fdecf0a1425`  
		Last Modified: Tue, 04 Oct 2022 23:54:10 GMT  
		Size: 52.7 MB (52699992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf11604dc48e052d8e37eb1cc1dfe25e82ca0599fa2d1cde4caa1641ef6c54c`  
		Last Modified: Tue, 04 Oct 2022 23:54:36 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:df95bcc6320309e64baa5d350246a2d1ea5553febb15c8c6c8d0fdea9418677e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51625570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e6afff69a33782312d560d5df9b739837f00251e626204833d8e946c15f22f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:24:49 GMT
ADD file:4aeae93f89cf412ab09736d5ac5f3af3efe3032bdb4dd76d8e3a2ac456687adc in / 
# Tue, 25 Oct 2022 02:24:50 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:25:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16cac6c5545e42023b7794a8dbcc0ad9450fddbb0d09c1f1cab8dbb35b922f49`  
		Last Modified: Tue, 25 Oct 2022 02:32:17 GMT  
		Size: 51.6 MB (51625349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf9311a48fc4e09c9ff181482add905186f84a7e2de6c0b49a4855d415109f0`  
		Last Modified: Tue, 25 Oct 2022 02:32:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:1055ee96fb4aa40bfb557705ff53f831bcfb25d2907570c3d95610b0c841f7b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52670214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a02c4ecaf7b61d170a5a174872007057379522634797acba9c41cf245d026e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:30 GMT
ADD file:f58a52903d9fd354b39418705999d807d445923c0d906e435069da0c1dcadb52 in / 
# Wed, 05 Oct 2022 00:14:35 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:568a1dbbc77ecb3e3f3c1bf7be75c0c5280b3cdd49fab44535b884d882f46658`  
		Last Modified: Wed, 05 Oct 2022 00:23:09 GMT  
		Size: 52.7 MB (52669989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36626a52a725d49f5c27919c9cba031479c302e31f98d7ee8a58bb1eec3e1f11`  
		Last Modified: Wed, 05 Oct 2022 00:23:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:05860fcb387be331288a6666682a57b04c641bce49e6b8fb8ca412b9d879397f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54704979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1960b0d33ef2ce53e8873deeed9aa16e9de0ab1fd1135d10d9286cb0250deaea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:54 GMT
ADD file:e0bb372ce8536511226fcc88c3a41d46e9ca8d9cf36d60b0c428dff4609ca95d in / 
# Tue, 25 Oct 2022 03:15:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:af67c63cd159199f43d062831737315a1baa10378f9e929485c676a22a4f621f`  
		Last Modified: Tue, 25 Oct 2022 03:22:34 GMT  
		Size: 54.7 MB (54704757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfe3670cf7e57dff797b7b1a81b3e236d3bc10620cb6e15a6dffdc555156ee3`  
		Last Modified: Tue, 25 Oct 2022 03:23:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:b082869078579995aa16eeb74f8ac655b4a51d91b4eb9e7aad33cb7752b3d2a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48857998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae6beb27df1abcddfbe6a029718dc63ec2a09e72e74f7aa6e23438ae91bdbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:43:33 GMT
ADD file:c69bdba9cce2cc03f2cfd44cc313597fa4405db3fb0eccb433d88722ab31e34f in / 
# Wed, 05 Oct 2022 00:43:35 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:47:15 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ceea310cdd06f4830c3118154bafc9f92a2a516a584c58091678a3121e2aeb79`  
		Last Modified: Wed, 05 Oct 2022 01:02:00 GMT  
		Size: 48.9 MB (48857770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe922ddecfa6a280e6520a82797a6ea2b614196d9919da35bf2b800c0a7510a1`  
		Last Modified: Wed, 05 Oct 2022 01:05:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:3696bfecd4373574428052be1c6bc57f86857903acb5c6b86fb7b0ae9031fb86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49013157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b736aeeda8a8eee6fc99797030aedd3efd0c0f0c53950bbb63d4993259e6f5bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:16:15 GMT
ADD file:0258dcf1ca7bf72abeb6bb2a139a712f118544a38e38c277acaae984d4312e12 in / 
# Tue, 25 Oct 2022 01:16:17 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:16:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ad8b0151e3d93e0406fa9194bfc8fabf5a340300bed913637542073f2f8b0eb8`  
		Last Modified: Tue, 25 Oct 2022 01:20:42 GMT  
		Size: 49.0 MB (49012938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb1bf872871a010d0b98d4063c2111eaedaa5837abc609668142bdd837da14`  
		Last Modified: Tue, 25 Oct 2022 01:21:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
