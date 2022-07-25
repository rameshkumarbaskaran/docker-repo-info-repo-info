<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:9e59137405de53b39517c969f3db72aa908ca47aae80cfc0eef044d6667a6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:835f433b433eeabe2dd7b84437bf68821de88d919b74dfe926a8d873b279ec14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94802599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5be7550a979a067733f202754a3d1a839aa0b7430f08de6413d44279738b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Jul 2022 18:23:46 GMT
ADD file:c14e9eb3157989efb62a3ae2adbedd897c4fd3d5c56da796e8863671bd96bf43 in / 
# Mon, 25 Jul 2022 18:23:47 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 25 Jul 2022 18:23:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1c048e3b6cde2ead574fae76c86cb11104421a8d247c1705accec4b4b11f823a`  
		Last Modified: Mon, 25 Jul 2022 18:24:11 GMT  
		Size: 94.8 MB (94802381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e711362fcd07df1ac9dc0f4ec1738b742c509c1516f20804fd35e88bb6444de`  
		Last Modified: Mon, 25 Jul 2022 18:23:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:9e59137405de53b39517c969f3db72aa908ca47aae80cfc0eef044d6667a6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:835f433b433eeabe2dd7b84437bf68821de88d919b74dfe926a8d873b279ec14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94802599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5be7550a979a067733f202754a3d1a839aa0b7430f08de6413d44279738b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Jul 2022 18:23:46 GMT
ADD file:c14e9eb3157989efb62a3ae2adbedd897c4fd3d5c56da796e8863671bd96bf43 in / 
# Mon, 25 Jul 2022 18:23:47 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 25 Jul 2022 18:23:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1c048e3b6cde2ead574fae76c86cb11104421a8d247c1705accec4b4b11f823a`  
		Last Modified: Mon, 25 Jul 2022 18:24:11 GMT  
		Size: 94.8 MB (94802381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e711362fcd07df1ac9dc0f4ec1738b742c509c1516f20804fd35e88bb6444de`  
		Last Modified: Mon, 25 Jul 2022 18:23:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
