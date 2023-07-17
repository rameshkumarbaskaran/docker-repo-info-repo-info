## `archlinux:base`

```console
$ docker pull archlinux@sha256:fe6b55ecfcfe638aa13560cdc66eb2ad9bd6c4f6684d27d0d2a3816cf2882a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:cf219c9214e840f642076be8eac01509e83fd2ccf540d3f416cd2384c7ebc479
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146733218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83177fd64f444d3690ca73822bb6ad6ab9bb4ad0b9cd250f8b9aa799699d8897`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 17 Jul 2023 19:19:59 GMT
LABEL org.opencontainers.image.version=20230716.0.165339
# Mon, 17 Jul 2023 19:19:59 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 17 Jul 2023 19:19:59 GMT
LABEL org.opencontainers.image.created=2023-07-16T00:07:26+00:00
# Mon, 17 Jul 2023 19:20:05 GMT
COPY dir:fec049f813929c8d117fc0b91fbcb51f942d7862d35c7a93f869983773bfe470 in / 
# Mon, 17 Jul 2023 19:20:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230716.0.165339' /etc/os-release
# Mon, 17 Jul 2023 19:20:07 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jul 2023 19:20:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f0e8ad11b5eaa0bc7045700a7c25289b34e613f54b06c33d70288ece0e8d8a8`  
		Last Modified: Mon, 17 Jul 2023 19:21:53 GMT  
		Size: 146.7 MB (146725130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b7449698b12238d1c52d4c41cfe36a6cd5bbbd57a727ab4babe84c18dde04`  
		Last Modified: Mon, 17 Jul 2023 19:21:33 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
