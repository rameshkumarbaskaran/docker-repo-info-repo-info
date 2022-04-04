## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:ed358bac5309a9e9377642f7c1686b2a7256eaff1f1367e0b3d733b657167913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:045fd14291db02e8eca5366aff97e56b70111f9c77fd6479b330db9ce27bbfff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88012346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd80aec208038fe3ab07dda50deec0d7497aa358a8abc30660fca79a54a0872`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 04 Apr 2022 21:43:04 GMT
ADD file:a9210c0d10f92b1e272ef8f8655ee9ef220447138220f04a1c9f6fb6ebc4cc0d in / 
# Mon, 04 Apr 2022 21:43:05 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 04 Apr 2022 21:43:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1fa2a347efd179bac92be1b07c1465823697604e1dfe7df67abc104ad09fe605`  
		Last Modified: Mon, 04 Apr 2022 21:43:25 GMT  
		Size: 88.0 MB (88012130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e66f6f5c6c32c6478d3bd7b266a896c570e4d955214e7dcda0a6afe1467eaf`  
		Last Modified: Mon, 04 Apr 2022 21:43:13 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
