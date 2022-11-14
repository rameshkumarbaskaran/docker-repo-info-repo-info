## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:10bed2d70017b05058cb54dc9efe92597ffbcf151c841043ff0d54e5c71b50ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:8f7920c2ef29805016f60380740501223ce111ce6c123bee35eba7b321442cc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67722169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571099f2b16cca84a6689cca6a76cb0d5aa3d751eda39af3edb33ee5c145b9a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Nov 2022 22:33:38 GMT
ADD file:485d958da241f92c275d8b644e20bcfc3e5c8684ca73344d0728755bc18d2eb0 in / 
# Mon, 14 Nov 2022 22:33:39 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 14 Nov 2022 22:33:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4557a4d4f515ab9778f1be2ff943edddb7cd5d6b6ce8f2b03548866acb39cb56`  
		Last Modified: Mon, 14 Nov 2022 22:34:00 GMT  
		Size: 67.7 MB (67721952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143ec0408f8d6f4a6f51be3247b4363df196c7c44e3400e82d74f1dca0a9492a`  
		Last Modified: Mon, 14 Nov 2022 22:33:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
