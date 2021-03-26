## `debian:stretch-backports`

```console
$ docker pull debian@sha256:6d057a03396efec6036a2d1be4c6f83211380d5b34f0118f05c073612d7e6145
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
$ docker pull debian@sha256:2a3590c93b7b7982c2ad57aa6b46bdb92d10a9f6412b87044834009569638ea7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1733b51159b7d99067a37d7c911b673964b284fb7c1a6ae498a9067d2ebe7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:22:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330e7ea58e4af6499e4e9ba3b7a87029d915771fdcf19b3b871473e15ca4d7a3`  
		Last Modified: Fri, 12 Mar 2021 02:30:13 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:6f87f836b8f19ee612032b57c8feb62529b948c3ee41b07e0c377c03607d3d96
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70ec49ee2888eea1a5b355effaa15d4bf5d25dd29f8151e7bcf0cf355336dff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:57:02 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f72e89ea7c437565a52b42c4e9da63017ec80aba28c507a1e9d125244c712c5`  
		Last Modified: Fri, 12 Mar 2021 02:04:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:eac30a44a67d084fd8290223ecd744069688649f88dfd541af11a1e14424e0a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4077e24ff9568dd079191e4db7acf9f13a98b8b55ac167cfb33f88d8a282e9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:46:49 GMT
ADD file:d375b61a6f54e93dae847e774b9d2de9027e20c5f667a979ba3312db2b3d75d8 in / 
# Fri, 12 Mar 2021 01:46:49 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:46:57 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a64dc3d1f8db8956691dfe60610f75a02084f49c3957d062b676c6baf818ffa1`  
		Last Modified: Fri, 12 Mar 2021 01:56:33 GMT  
		Size: 46.1 MB (46098170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c2640959eb4ce5f5f29fb07ab9c4cf80691e4abaf816c95cffae7abbc27d40`  
		Last Modified: Fri, 12 Mar 2021 01:56:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
