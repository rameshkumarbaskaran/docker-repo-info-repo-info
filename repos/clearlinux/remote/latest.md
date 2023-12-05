## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:fac2a9207acd4a7eb2b42a270bf1b244bd61fcf383cb937e715922ed0dabf46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:57900f9bf6a8a6e1c1365f723969fe8aef76acffeb2b55e185fc87ce1db2fc96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68058027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3be36c280f5c489a60b30f3d6e418d3f77fdee1d89d643d1fbee841502e63c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 05 Dec 2023 00:22:35 GMT
ADD file:17ee1ad4e0a21f1c12aa6deb8c0281dd32a4449b0cd75abdbb000fade83dc4c0 in / 
# Tue, 05 Dec 2023 00:22:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Tue, 05 Dec 2023 00:22:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd447bc3acfa3a0482a6b2833407886c3140dca3d7947c5feac121179afb2`  
		Last Modified: Tue, 05 Dec 2023 00:22:52 GMT  
		Size: 68.1 MB (68057816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6aaec2c8082106581574b46a50515fdb6f7c2c27e67981102c3481108ebf3d`  
		Last Modified: Tue, 05 Dec 2023 00:22:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
