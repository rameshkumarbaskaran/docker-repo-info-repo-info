## `debian:experimental-20221024`

```console
$ docker pull debian@sha256:fa11024fc92b86322a46f9389dd0e2ff17536c6ca00a2a91c3415982997106dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:experimental-20221024` - linux; amd64

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

### `debian:experimental-20221024` - linux; arm variant v5

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

### `debian:experimental-20221024` - linux; arm variant v7

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

### `debian:experimental-20221024` - linux; 386

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

### `debian:experimental-20221024` - linux; ppc64le

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

### `debian:experimental-20221024` - linux; s390x

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
