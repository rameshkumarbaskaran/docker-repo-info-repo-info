## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:10d05806f5ab14b5630ca80951e291bfc840c5989ce011594f387b08263a6fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:cb08e2ce287c30f5484e0264132e697fb36f01734c9489492ff5c3f3db729812
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6900859077b5b71e6ca72c31a5a2c62e41f96081aea5f2cad117e5c5e48f06`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:16:57 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:16:58 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:16:58 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:17:09 GMT
COPY dir:26a13fc3a1ba45fe2c4b0785d8b1a68ce5991bc4fbd4c078f8b86bf9c621781e in / 
# Mon, 01 Jan 2024 19:17:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Mon, 01 Jan 2024 19:17:12 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:17:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:444f393ce858c4b3035c5cb5e2e6b5b46661dd73311818d48dead4150ac68209`  
		Last Modified: Mon, 01 Jan 2024 19:20:00 GMT  
		Size: 266.2 MB (266229441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86584fa290cd875121991e41d307669a30794663283b8ae95a85ea8b6f751987`  
		Last Modified: Mon, 01 Jan 2024 19:19:23 GMT  
		Size: 8.9 KB (8950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
