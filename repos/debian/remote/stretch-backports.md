## `debian:stretch-backports`

```console
$ docker pull debian@sha256:1f167c8d807f40c58a8cb4b66b1dc72001538885c6240f7cca6e398ab0d97ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:24242f53ccd01babde8aab23b96700d5fe79a2757aa7cfa6e2c57eb4957df1e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45379736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62d1c5815c9310b5411e7fd4f46e8a6829e0ddda74f422a8ad95aff50403ddf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:23:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f28d58d1b0f2a62c288a18c914cc3cf0f8f02a717aecc924017c5ca16dad9b`  
		Last Modified: Fri, 26 Mar 2021 15:32:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9439360a7ae27fb79d9c9b556dac5689d9090ea4343066536f3fe5799e2b3289
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc9844da92ce673ff01572214037cf46ec3b92de28d12a6145528c0324cb418`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:55:39 GMT
ADD file:ba0bcff641608b2668ebc0a0a795d8bd32a275ee0bfd9e161b43fafccfa96545 in / 
# Fri, 26 Mar 2021 07:55:44 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:55:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7298374463f66e0dde12fde13b833e7f90c3f9d526420eb8a6f05dbbe3600d69`  
		Last Modified: Fri, 26 Mar 2021 08:04:13 GMT  
		Size: 44.1 MB (44091954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b812da25f96002ff7a85cadfdb71ae8da9d17bebd837aa0501663ba21a020`  
		Last Modified: Fri, 26 Mar 2021 08:04:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8a260a41cf04708ff8ebee3c5b7aac5ae54fa34915faaa099db35e818259240e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8325203b9f94f18218a478d6cc2644265bff068bb416afc54b5ecf7051792`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:16 GMT
ADD file:9ca2a8d5e2b8ba00bb66699e4970399555c20e8f9a4b8afa0b01076b90f0d8e3 in / 
# Fri, 26 Mar 2021 11:22:19 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:22:31 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:011348b3c4acf7cfad3a8899e3a5f135377a30045eb428e4d759ef7e138740b1`  
		Last Modified: Fri, 26 Mar 2021 11:31:14 GMT  
		Size: 42.1 MB (42119842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b4800c0bcc560689cec1f9b0f8252e31b131d2c91c0f0d77402c1f442ca6e6`  
		Last Modified: Fri, 26 Mar 2021 11:31:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0e6a76d2e3da3871e10669eca8f1b44e03e09974087372f5bc75fb63bef40cdc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43176630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449956e1925574b009852893de3a1916fe4efbfe78f73f66bd7dc5a15d205b4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:44:28 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb269c68f59520e3ccad57a25fc43d88b9dfaf3e446fe6764bb80a3e0a986b70`  
		Last Modified: Fri, 26 Mar 2021 15:51:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:03b72f0e1ce1b244bfb30c341ce4420a96253fe490334542828df5a9b53fcf88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53654f6347590ccbe0eb0a283c45049744304ce8628e4d78d9c318e2dd31475`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:55:57 GMT
ADD file:0a48869723941cb015604aec94e5f955449b86eca7c73ec978c3d1dcaf3517ba in / 
# Fri, 26 Mar 2021 13:55:58 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:56:06 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01c2b0829d8abcf8cd9012766b99919fd21d4a2c1fae4d9312b5716bf40ba27e`  
		Last Modified: Fri, 26 Mar 2021 14:06:26 GMT  
		Size: 46.1 MB (46098430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce9f445152c7aeacdf60aee16feb49e3e79aab3a040bef2944f5633e47af634`  
		Last Modified: Fri, 26 Mar 2021 14:06:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
