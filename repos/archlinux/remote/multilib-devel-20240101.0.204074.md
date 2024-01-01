## `archlinux:multilib-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:bb3a985537eb8d330ddeeba7cc2dfdcccc966e52041cd3604ed41ba57d53bba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:multilib-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:9568db8e73f27e9df3523ce67329fbb276469d31f0201584747107dfb1188aea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316045027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c19037da711e1f7e945906d366095fdd53addb2c33e5f538d42d0b43a70cf56`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:18:16 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:18:17 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:18:29 GMT
COPY dir:75c66889520f549930c0f406d7a42c7d20e2d1d2e662322c69dc3a2dcb5d5bc5 in / 
# Mon, 01 Jan 2024 19:18:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Mon, 01 Jan 2024 19:18:33 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:18:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f377e15cb8d612a50f6c51ebcee45ab2e4b9221e4dc99f177dc54b529f9f0edf`  
		Last Modified: Mon, 01 Jan 2024 19:20:55 GMT  
		Size: 316.0 MB (316034966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a18e0da136cad75444612824bd9fc1be654c87e5c95cecec6ad5bbbab563fe`  
		Last Modified: Mon, 01 Jan 2024 19:20:12 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
