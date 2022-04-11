<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:1d64e1c6d65d04a2b02b38ec545c78fdc1897e7ec4b43ba667c6eaa3bda3341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:bceb35dda79bd2740d179600eaacfe42cd58f17f9eaf8fb7ae1f99a560721bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88216478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5683ac34fe461c2dfc6579dd21aca9acae59771aa23a9ac465dc7d504e925604`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Apr 2022 19:23:31 GMT
ADD file:9f91b7cee401d23880823ca512a38bad026e96ade646dd4f0c023567415f8e0e in / 
# Mon, 11 Apr 2022 19:23:32 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 11 Apr 2022 19:23:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c55b5eef5f7c1c33b4b68c11d9bf09215dcce95c76535aa2b35f37512c135a2`  
		Last Modified: Mon, 11 Apr 2022 19:23:54 GMT  
		Size: 88.2 MB (88216261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaad5773ef3952b0ba7b4bed519c2b9432971b960cc4a9a2455ec87174c7daa`  
		Last Modified: Mon, 11 Apr 2022 19:23:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:1d64e1c6d65d04a2b02b38ec545c78fdc1897e7ec4b43ba667c6eaa3bda3341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:bceb35dda79bd2740d179600eaacfe42cd58f17f9eaf8fb7ae1f99a560721bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88216478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5683ac34fe461c2dfc6579dd21aca9acae59771aa23a9ac465dc7d504e925604`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 11 Apr 2022 19:23:31 GMT
ADD file:9f91b7cee401d23880823ca512a38bad026e96ade646dd4f0c023567415f8e0e in / 
# Mon, 11 Apr 2022 19:23:32 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 11 Apr 2022 19:23:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c55b5eef5f7c1c33b4b68c11d9bf09215dcce95c76535aa2b35f37512c135a2`  
		Last Modified: Mon, 11 Apr 2022 19:23:54 GMT  
		Size: 88.2 MB (88216261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaad5773ef3952b0ba7b4bed519c2b9432971b960cc4a9a2455ec87174c7daa`  
		Last Modified: Mon, 11 Apr 2022 19:23:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
