## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:59f033e333e97e9350f267718f0f691ef4ad2e48d354d58e8507e8a1ecbe78d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:703b9d73d29dbe60355d9ecf0fe6314451ab05477344d7fe427c438d1fb175d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84439900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29ed0148a16f228f641cf237dcc5523e4b7cdaa95a7dd7ce6134780a0628a31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:45:45 GMT
ARG RELEASE
# Tue, 09 May 2023 12:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:45:53 GMT
ADD file:87293581d53f522106a37eee2d3056cd4d9bdbb4a58077389c817bd655a4e0c7 in / 
# Tue, 09 May 2023 12:45:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:54:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e685e76ac424b804c8b8208c603584b34300a955516eaff83d30f060189f522b`  
		Last Modified: Tue, 16 May 2023 23:59:49 GMT  
		Size: 27.0 MB (27026748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd2979a9c21a4b382153460cb77e2f6d383b4c4cb5cdeb37baa35c84e174a1`  
		Last Modified: Tue, 16 May 2023 23:59:46 GMT  
		Size: 13.4 MB (13350711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342807f1db024cabeca1aa775473201ce240f01d11faabb59c89f443a7bc8cad`  
		Last Modified: Wed, 17 May 2023 00:00:03 GMT  
		Size: 44.1 MB (44062441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21a95cdd7cbd011e112f406d36a23f51265a389f8f0b04923caee0cf7216dcce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84351533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6b3b9deabe2fa382fac07948bb15670db21d8aef8e165bb8b017a3fbac4983`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 13:09:19 GMT
ARG RELEASE
# Tue, 09 May 2023 13:09:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 13:09:21 GMT
ADD file:a5ed2ab846477e26003abb09795ef405e1d96bec9be1a3cb0b258dd5aa83f075 in / 
# Tue, 09 May 2023 13:09:21 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e21501268ba0e8cdc7e0134b231643691b6d4648511a6bbed295eeca807810d8`  
		Last Modified: Tue, 16 May 2023 23:58:10 GMT  
		Size: 26.2 MB (26239447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b45801daded85936f7c762c0148a3d71e35c237bfe96ba49811f0964c16cb9`  
		Last Modified: Tue, 16 May 2023 23:58:08 GMT  
		Size: 14.0 MB (14018228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1711be48a0a429b31d94131f11f34c0b5f5eb3de15640bbda8ad0c25bba80a0`  
		Last Modified: Tue, 16 May 2023 23:58:21 GMT  
		Size: 44.1 MB (44093858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
