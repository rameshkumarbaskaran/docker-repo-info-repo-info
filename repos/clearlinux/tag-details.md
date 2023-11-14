<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d18e3b33ef6531f6e52c3b25257775920a6b0a90fafac61d0e46102d74311c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:08c904fcfc0a85120a10161640a43cbb3de56c278ba4aa2ee428afa13c4afcbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68034856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43f6b95fd412c6c4c4fae29afad838ba9965b5f0ba97967e5c0b95957655d10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 14 Nov 2023 00:33:00 GMT
ADD file:4b8ea81e289e645195b6bc87ef11a86e068639686f926f3cfd3e6bfb2c94dfe1 in / 
# Tue, 14 Nov 2023 00:33:01 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 14 Nov 2023 00:33:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3017a272d1d570a5bbc64cb4b419c3112b314d14f25320b340ac5a7edfa863f6`  
		Last Modified: Tue, 14 Nov 2023 00:33:18 GMT  
		Size: 68.0 MB (68034643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe8269f82f359656c8bf8e0400c29e453808b0b21e7dec42305c4eb64802195`  
		Last Modified: Tue, 14 Nov 2023 00:33:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d18e3b33ef6531f6e52c3b25257775920a6b0a90fafac61d0e46102d74311c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:08c904fcfc0a85120a10161640a43cbb3de56c278ba4aa2ee428afa13c4afcbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68034856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43f6b95fd412c6c4c4fae29afad838ba9965b5f0ba97967e5c0b95957655d10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 14 Nov 2023 00:33:00 GMT
ADD file:4b8ea81e289e645195b6bc87ef11a86e068639686f926f3cfd3e6bfb2c94dfe1 in / 
# Tue, 14 Nov 2023 00:33:01 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 14 Nov 2023 00:33:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3017a272d1d570a5bbc64cb4b419c3112b314d14f25320b340ac5a7edfa863f6`  
		Last Modified: Tue, 14 Nov 2023 00:33:18 GMT  
		Size: 68.0 MB (68034643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe8269f82f359656c8bf8e0400c29e453808b0b21e7dec42305c4eb64802195`  
		Last Modified: Tue, 14 Nov 2023 00:33:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
