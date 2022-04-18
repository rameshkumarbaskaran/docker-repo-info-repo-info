## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:142585bd9de54db1fcc613335b22b8f8fd55b39c7cc2518a6f17f4f2d298a66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:222ba85783c27e93550cdb3cf35f1e204bfae63d0b3fd803bd16f203c8fe4485
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88171104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8303166f4194af733c5e35885707973ac645b4a2978876093f768fefa146a05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 18 Apr 2022 18:23:04 GMT
ADD file:7d07ad8311df0d6fbfd2662aea180adf39ea3fc09f08a770708168ccbd01a202 in / 
# Mon, 18 Apr 2022 18:23:05 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 18 Apr 2022 18:23:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ac6b742ad1c1480ef0ea2dfc7c38979dadab89b1d5586320657991dad7d4858`  
		Last Modified: Mon, 18 Apr 2022 18:23:26 GMT  
		Size: 88.2 MB (88170887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aefa8d52ab54c5ef5d9d78e3f91134ece04656f3e2d3b2066f3d9acb3502ae1`  
		Last Modified: Mon, 18 Apr 2022 18:23:14 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
