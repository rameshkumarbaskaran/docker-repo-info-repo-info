<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f0ef7569ba89195f649eec572a7ed6bf70e61c9fc7dcd24c5bc069e8211d1fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:cca6467763f31e630e56101665958ab2a7ec424cf2cc57aee209609b9562188e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68823672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7570ee44b5d25e97f74d2275d5c0bdef4e6a8f10273a9cf6357f26183b8bd6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 17 Oct 2022 20:23:49 GMT
ADD file:524c5a931c671d996ead59327c35c6cb8031cff1ad5b2763c302b16ab3e8b1d5 in / 
# Mon, 17 Oct 2022 20:23:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 17 Oct 2022 20:23:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1c76838b82864f8ac4a60d61e529b1b5da70880be3f50416e82de6896f9903ed`  
		Last Modified: Mon, 17 Oct 2022 20:24:10 GMT  
		Size: 68.8 MB (68823454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d8e21fc7fc76da8d9c5f48794e899d832ea65c42a7102ad33afa7cf22a356f`  
		Last Modified: Mon, 17 Oct 2022 20:24:00 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f0ef7569ba89195f649eec572a7ed6bf70e61c9fc7dcd24c5bc069e8211d1fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:cca6467763f31e630e56101665958ab2a7ec424cf2cc57aee209609b9562188e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68823672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7570ee44b5d25e97f74d2275d5c0bdef4e6a8f10273a9cf6357f26183b8bd6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 17 Oct 2022 20:23:49 GMT
ADD file:524c5a931c671d996ead59327c35c6cb8031cff1ad5b2763c302b16ab3e8b1d5 in / 
# Mon, 17 Oct 2022 20:23:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 17 Oct 2022 20:23:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1c76838b82864f8ac4a60d61e529b1b5da70880be3f50416e82de6896f9903ed`  
		Last Modified: Mon, 17 Oct 2022 20:24:10 GMT  
		Size: 68.8 MB (68823454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d8e21fc7fc76da8d9c5f48794e899d832ea65c42a7102ad33afa7cf22a356f`  
		Last Modified: Mon, 17 Oct 2022 20:24:00 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
