## `archlinux:base-devel-20230723.0.166908`

```console
$ docker pull archlinux@sha256:4a5ba44e5cb4bf49932da6d2ba9dbdb04ac6843fe40568c5479a218e6163b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230723.0.166908` - linux; amd64

```console
$ docker pull archlinux@sha256:0177814601cc10b58d4364bb790c8ce0c17db10d48a7c8da54a1f697253159e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263720287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51879f7f2befde96ccc332d360e00da3159a6eb351cd65e046307eb66fe1c74a`
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
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.version=20230723.0.166908
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.created=2023-07-23T00:07:51+00:00
# Mon, 24 Jul 2023 22:20:58 GMT
COPY dir:0b871f5e73e52537b3829dfbffbd8ef04e46de7d619959305deb2d62e1d8e596 in / 
# Mon, 24 Jul 2023 22:21:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230723.0.166908' /etc/os-release
# Mon, 24 Jul 2023 22:21:01 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jul 2023 22:21:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7db0a613b381eb6bf1765e6d2670a1d1e353b8bcfb7effef0675494727728006`  
		Last Modified: Mon, 24 Jul 2023 22:22:27 GMT  
		Size: 263.7 MB (263711445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549be721c1ee7c45a29e67e47ab6ec2608500d98dd3d436547da2e6f8ebc7a6`  
		Last Modified: Mon, 24 Jul 2023 22:21:52 GMT  
		Size: 8.8 KB (8842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
