## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:6696778ef393c161d8294924b11317eaf278c36ffcc129b64796334afb73c3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:b0a3383d429410ffb779d3375454ee3c3ec04912f60931ca163b90af46f2148c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67793833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e189d768cb1e8a6f442e9c27556a492922887dee7095e3d3c9cd8c58954c26`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 19 Dec 2022 21:23:06 GMT
ADD file:db7b86ec4660e288aa68c844237e8762d922f8cc4d5bf204141faf9fa9d0cb64 in / 
# Mon, 19 Dec 2022 21:23:07 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 19 Dec 2022 21:23:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5fbbd7bae51be1f95d1134f9221eed44ca47978148582d0ab5414bc32f59edf5`  
		Last Modified: Mon, 19 Dec 2022 21:23:25 GMT  
		Size: 67.8 MB (67793615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2392c64f69f9c734517d36fb6cdfbb4cc99613f5a1df4359c1e503fb3d26d`  
		Last Modified: Mon, 19 Dec 2022 21:23:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
