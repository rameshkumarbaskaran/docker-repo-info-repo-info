<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:5480787b6a1c95f2ebd99585254e4bdaf78368efbac6f012cb4ba734437e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:ce30d7099c3c578f51e9e56d0ebad5326185bd05e3f72d9d96f4321812af0dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67725157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe884dce8b272348474ef98f08701eddedf79333b0ba3f9dadde2b5078c18f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Nov 2022 19:24:34 GMT
ADD file:447f044e721be3546547dab2a58782e07c9a27a54075518ff5d0b5e040f95e61 in / 
# Mon, 21 Nov 2022 19:24:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 21 Nov 2022 19:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db59ee456d754c884f9b7e824735245f124add670d009289ae6ae5de4242ff80`  
		Last Modified: Mon, 21 Nov 2022 19:24:55 GMT  
		Size: 67.7 MB (67724939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430b911791893730baaa5db777bb81184cdcd6428fdfe68d760a4d02b2082e4b`  
		Last Modified: Mon, 21 Nov 2022 19:24:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:5480787b6a1c95f2ebd99585254e4bdaf78368efbac6f012cb4ba734437e5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:ce30d7099c3c578f51e9e56d0ebad5326185bd05e3f72d9d96f4321812af0dbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67725157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe884dce8b272348474ef98f08701eddedf79333b0ba3f9dadde2b5078c18f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Nov 2022 19:24:34 GMT
ADD file:447f044e721be3546547dab2a58782e07c9a27a54075518ff5d0b5e040f95e61 in / 
# Mon, 21 Nov 2022 19:24:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 21 Nov 2022 19:24:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db59ee456d754c884f9b7e824735245f124add670d009289ae6ae5de4242ff80`  
		Last Modified: Mon, 21 Nov 2022 19:24:55 GMT  
		Size: 67.7 MB (67724939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430b911791893730baaa5db777bb81184cdcd6428fdfe68d760a4d02b2082e4b`  
		Last Modified: Mon, 21 Nov 2022 19:24:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
