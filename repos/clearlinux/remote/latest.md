## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:3eb8a887c60edd8229aa575e61621f4dbb2d4c390583788b57231cd0fdf1a86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:084f2ca03ff7932e2b5780dfc46aa8483ebd984e8ad7134372622b862fdcb66d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89719190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffa390544932da876670ee63d0f5ac52faa1dcda17d8ccfc114c5a6a2a3b755`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 30 Jan 2023 20:19:28 GMT
ADD file:eb86d4786ffab9c071bfd71facbaceaf3077b0efd40b75278cc2474c9a329ac3 in / 
# Mon, 30 Jan 2023 20:19:29 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 30 Jan 2023 20:19:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7db65f1552383c38b37d2188a84444f50f9dddb4c3abb250a051b95e8a72af72`  
		Last Modified: Mon, 30 Jan 2023 20:19:53 GMT  
		Size: 89.7 MB (89718972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a4bda222953e7d100927169d3aaca509fe82d9d87997b2c9292884bc9c9891`  
		Last Modified: Mon, 30 Jan 2023 20:19:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
