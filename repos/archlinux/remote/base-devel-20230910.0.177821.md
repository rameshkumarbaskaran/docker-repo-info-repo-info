## `archlinux:base-devel-20230910.0.177821`

```console
$ docker pull archlinux@sha256:670588c2a31489cebb4a7d18601f4b689a07df98d5735625e89d3a4e39c7423c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230910.0.177821` - linux; amd64

```console
$ docker pull archlinux@sha256:14b92175bb6e95c3fb19e246a61b6d701cfb8dce2fae097e34b5c071c4b7e690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265758388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d90f1b9e54ba5e3404d5048c353d5d94fdbc4324383439383d75f6db6d41a1`
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
# Mon, 11 Sep 2023 19:20:48 GMT
LABEL org.opencontainers.image.version=20230910.0.177821
# Mon, 11 Sep 2023 19:20:48 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 11 Sep 2023 19:20:48 GMT
LABEL org.opencontainers.image.created=2023-09-10T00:07:33+00:00
# Mon, 11 Sep 2023 19:20:59 GMT
COPY dir:a3e677a95bda2b40e12d7e95e8eb5a4ad3b05bd99a59def2370f285453f42192 in / 
# Mon, 11 Sep 2023 19:21:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230910.0.177821' /etc/os-release
# Mon, 11 Sep 2023 19:21:03 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2023 19:21:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3b641bfcabf54096189d03ddc03300b7d2907393a4db60b40d974bc1d032fc72`  
		Last Modified: Mon, 11 Sep 2023 19:22:32 GMT  
		Size: 265.7 MB (265749482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd852543772e5f7cec33ed957788a284455f79f9509de8596b60abd6d059701`  
		Last Modified: Mon, 11 Sep 2023 19:21:53 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
