<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240101.0.204074`](#archlinuxbase-202401010204074)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240101.0.204074`](#archlinuxbase-devel-202401010204074)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240101.0.204074`](#archlinuxmultilib-devel-202401010204074)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:fed6efe803e79d94544f93607e4afec1056cfd9bee5744c965eec0944624d81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:73e7485d52a63bec319bae1795522dd738d12cfb45ac345b166080783bf3a5ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f38d8f6347d027696923f4bfad86a036c5d9e67d717a7354d5f9216ea0bbd5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:15:57 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Mon, 01 Jan 2024 19:15:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Mon, 01 Jan 2024 19:15:59 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:16:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f82ee8a39c5c15c641d1f420c193622b3d6e32716c90d7bf663111d1bedf2f`  
		Last Modified: Mon, 01 Jan 2024 19:18:52 GMT  
		Size: 8.1 KB (8115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20240101.0.204074`

```console
$ docker pull archlinux@sha256:fed6efe803e79d94544f93607e4afec1056cfd9bee5744c965eec0944624d81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:73e7485d52a63bec319bae1795522dd738d12cfb45ac345b166080783bf3a5ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f38d8f6347d027696923f4bfad86a036c5d9e67d717a7354d5f9216ea0bbd5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:15:57 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Mon, 01 Jan 2024 19:15:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Mon, 01 Jan 2024 19:15:59 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:16:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f82ee8a39c5c15c641d1f420c193622b3d6e32716c90d7bf663111d1bedf2f`  
		Last Modified: Mon, 01 Jan 2024 19:18:52 GMT  
		Size: 8.1 KB (8115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:10d05806f5ab14b5630ca80951e291bfc840c5989ce011594f387b08263a6fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

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

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:fed6efe803e79d94544f93607e4afec1056cfd9bee5744c965eec0944624d81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:73e7485d52a63bec319bae1795522dd738d12cfb45ac345b166080783bf3a5ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f38d8f6347d027696923f4bfad86a036c5d9e67d717a7354d5f9216ea0bbd5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:15:50 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:15:57 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Mon, 01 Jan 2024 19:15:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Mon, 01 Jan 2024 19:15:59 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:16:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f82ee8a39c5c15c641d1f420c193622b3d6e32716c90d7bf663111d1bedf2f`  
		Last Modified: Mon, 01 Jan 2024 19:18:52 GMT  
		Size: 8.1 KB (8115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:bb3a985537eb8d330ddeeba7cc2dfdcccc966e52041cd3604ed41ba57d53bba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:multilib-devel` - linux; amd64

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
