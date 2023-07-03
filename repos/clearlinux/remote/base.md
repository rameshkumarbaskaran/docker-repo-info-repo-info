## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:49d59cc2d091c002979be1dd30811c319fba23ab982a65eda9f892581abdf5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:941a8842db16a2ea38d0ca2f4fec8ddf95e6eca8cbe3079fcf34b35ca8e68b35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72622610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc59212fa4623ab9c7b9d9c817dfa512e9daa29e37272deb35afef0b2117f056`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 03 Jul 2023 19:21:41 GMT
ADD file:0c59c51d4c264f6877dada447f9aa6d4bf02a1fe4268a97e112b3ad15ce1340a in / 
# Mon, 03 Jul 2023 19:21:42 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 03 Jul 2023 19:21:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6286daf11c6a8b56002a72ca3f966d7f99900d4a5ce219c7dd395dfdda90e630`  
		Last Modified: Mon, 03 Jul 2023 19:21:59 GMT  
		Size: 72.6 MB (72622393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f157f27c0aef1a2582f790725b77fdf6b0ee68d16a0be2795dcbc5ff94f85b7`  
		Last Modified: Mon, 03 Jul 2023 19:21:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
