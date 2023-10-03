## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:fa74cfcb8aabe2cb876a1a60820cd034f5a414b13007af1baacada18bb4c3812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:fa057a84079f77e3c6b1ad5dbfbf746e142a17ab41628efc4de96e20068c5678
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265017541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202c4d3d894a9fef928c732658e4edff7c4f7c9d85166264b13ff2fbcf8f515`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 03 Oct 2023 01:15:03 GMT
LABEL org.opencontainers.image.version=20231001.0.182270
# Tue, 03 Oct 2023 01:15:04 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 03 Oct 2023 01:15:04 GMT
LABEL org.opencontainers.image.created=2023-10-01T00:06:48+00:00
# Tue, 03 Oct 2023 01:15:15 GMT
COPY dir:df7a84e075b266176c1b425cffe2c107d700d5324f557b2192206d3496188524 in / 
# Tue, 03 Oct 2023 01:15:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231001.0.182270' /etc/os-release
# Tue, 03 Oct 2023 01:15:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:15:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4ad7f20d327af7b5423d91e6ad5705aeee891dd6dfbd41738cf3a60e59266462`  
		Last Modified: Tue, 03 Oct 2023 01:16:43 GMT  
		Size: 265.0 MB (265008607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59193466dab11fed768f5b6ac93b36771ff10b49c8c2cd6c34b81c88bff18e9e`  
		Last Modified: Tue, 03 Oct 2023 01:16:07 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
