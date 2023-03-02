## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:a758bfc450f945b672f492bc46e34e8fb7feec29946025e7df5085264377b78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f4779bb631cc96f8c601cb3cb2d4d19fc819689d534b0ec2049fb2aeb96b7e49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78694034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cccf588560d124231ebdcf5f275b4e27dbb214d9bf110989c70b375d2885f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:11:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:12:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7610e15a5bf822d71b65f5f7c7d873b70f585cebc9b4bfd76dedd61997f9e1c2`  
		Last Modified: Wed, 01 Feb 2023 18:23:55 GMT  
		Size: 27.4 MB (27419700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc4589b98247ebd93b0b4ca6c08ebf74c1fcb7fe81d1ee3a00ddd0381b99aaa`  
		Last Modified: Wed, 01 Feb 2023 18:23:52 GMT  
		Size: 6.6 MB (6635143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c87abeb95cddddf017930e8ffec58593bd520216c779b25e710376682a56c6`  
		Last Modified: Wed, 01 Feb 2023 18:23:52 GMT  
		Size: 3.7 MB (3690296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b97131389bee769ba93a32a51aee8b1f6fa2936b506cd9be1296fe2e9ef3d`  
		Last Modified: Wed, 01 Feb 2023 18:24:10 GMT  
		Size: 40.9 MB (40948895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:049d82e7a50c297020943bab44d6ae17ffc80d524d72a34544bdffde74443213
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83349017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaabfc7bbbedab1780b20eaee19155a1c5b9ebf58df1fc9f4f1df55b732b84e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
# Wed, 01 Mar 2023 03:01:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:01:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 03:02:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8391c317b70a65f7c7d5bf15686f27d06e2c79b286c3a86cb70987de2acdc4`  
		Last Modified: Wed, 01 Mar 2023 03:16:32 GMT  
		Size: 5.8 MB (5808831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd77c8b93dd4f4c7b1af018a1de3fc89606fac50a049b8ee85bd1ccd0335294`  
		Last Modified: Wed, 01 Mar 2023 03:16:32 GMT  
		Size: 3.9 MB (3851906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9367c233564b3534a29ad60c3843f0bbd6a4105cc65519f48f91cf119358142`  
		Last Modified: Wed, 01 Mar 2023 03:16:51 GMT  
		Size: 48.6 MB (48602279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4d2316040e83fb85fcf5553a00d9884e58bc4ae0ac45f809513198b31164f7a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81368243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78899799edcb9bb2076bbcfe6bcfb75f1dffa05836b5c21617593bc97cd03734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:30:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 02:31:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6700b5ef6bf750ef532062fc9dec24b7d9247840b877f26af1f339df77db5ba1`  
		Last Modified: Thu, 02 Mar 2023 02:39:03 GMT  
		Size: 26.9 MB (26899339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01eb5985b1759d7a00fafb6eaa0426c9ba33b24bab18656ae5ed19b74869bd3`  
		Last Modified: Thu, 02 Mar 2023 02:39:02 GMT  
		Size: 6.5 MB (6468687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5136aa3449032f883f29b10908230ca4a5c79c1a4fcf12f1c28fa763b07ac0db`  
		Last Modified: Thu, 02 Mar 2023 02:39:01 GMT  
		Size: 3.6 MB (3649336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99899628512ddfc061595eb4f812d31ea2842eb378a4f491eb3ab8c133270a51`  
		Last Modified: Thu, 02 Mar 2023 02:39:17 GMT  
		Size: 44.4 MB (44350881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a805a109b7caa13d3e7983ef1c11492c18454c10000ddc6c90fc09528e3427ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89714899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76476df3dde3cb0032f781c70db091e82cc22df5fee40845b4036edc34bda10d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:11:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Feb 2023 18:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5151cf1d3445f8b719163cb88c8ee7f7f2368e309dd1d14016546804fc05126`  
		Last Modified: Wed, 01 Feb 2023 18:22:34 GMT  
		Size: 32.0 MB (31980199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d337c3408ba6fc96792e39145bb0a122a3f04a96a5571d97c3f265402359009c`  
		Last Modified: Wed, 01 Feb 2023 18:22:28 GMT  
		Size: 7.6 MB (7605406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1579dbb09dc76707e4839919fcec93b48be4479e103cb1aeed1a50194d1724e8`  
		Last Modified: Wed, 01 Feb 2023 18:22:27 GMT  
		Size: 4.4 MB (4408979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f651ad714aac8d2542de9fc23ff6b10701efb943ac6c9538ea45be37d726bf0e`  
		Last Modified: Wed, 01 Feb 2023 18:22:57 GMT  
		Size: 45.7 MB (45720315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d2881270036984bf5335b8711121ff83ff86c5a2728ced037c770bedde7b192b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80403891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a23c0ce9ee9418f0b679ceeecc5514d7858bc439fcffeb582fb2d84c7f6a80c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:55 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:57 GMT
ADD file:88bec1acfbc8ba8a59354ff2c1f510d9e301748628aa39527cca86d8150209e8 in / 
# Wed, 01 Mar 2023 05:00:57 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:16:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Mar 2023 02:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e8382b8ddc15579f4e533ad8581d16988174176dacd958bc0572d8e6417518f`  
		Last Modified: Thu, 02 Mar 2023 02:24:57 GMT  
		Size: 26.1 MB (26072339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2428ddac9d5ad4baa24cd9a8735e4aa63591aa90c5e18869189f772ac106cd2`  
		Last Modified: Thu, 02 Mar 2023 02:24:55 GMT  
		Size: 6.3 MB (6319521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b57b8f1cbfb3971975200f23660e4e6bb616038be4ec693552ebd91f202ed1`  
		Last Modified: Thu, 02 Mar 2023 02:24:55 GMT  
		Size: 3.7 MB (3674671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f1225557f2081b054aaa9ce9fa92db7eaf86f05602bd00bb497082952dd77c`  
		Last Modified: Thu, 02 Mar 2023 02:25:13 GMT  
		Size: 44.3 MB (44337360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
