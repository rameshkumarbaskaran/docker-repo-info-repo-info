## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:f4fd1cbea3c5e3b5602ebeb693ed14a8df6dd42e1b1dae047d415580dc9eb7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9864a6a8920e10635a22be668dff1a9169c7e666efc7a51cf9cbd0fdacbd6a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41678109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c7af30dd7e2311fbf3138dfcad631878055c64260ae8f409b8c95880e15e2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4ae0f456d5b5ed53c0d0f67cd1948207060810837f2b15dcdf5bd97bbceb300`  
		Last Modified: Tue, 04 Jul 2023 03:56:47 GMT  
		Size: 27.5 MB (27488903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f7fd2e9f809d0b31bf96fde0b09fb68493e5499b9a4dae5f3dfc0a0ed0b7ce`  
		Last Modified: Tue, 04 Jul 2023 03:56:46 GMT  
		Size: 14.2 MB (14189206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f9d2ab3a6b2bfe19700d9a81e7879a756852897bb7e69ef593327222d0ff7a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39055297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b81c8de3b061bbd76bd5c96119fd3fdc21ae5a2825a6be253a88d2827b1adaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4bf34fad731c68e9e2b3f1ab9be267f88256224d876e0b36cd63ff42fe27225a`  
		Last Modified: Fri, 16 Jun 2023 00:58:56 GMT  
		Size: 25.9 MB (25914047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d88eb5459ee9fba90e6dc257e7e3002bdb40e23d679a15bf566ec317a366bb`  
		Last Modified: Fri, 16 Jun 2023 00:58:55 GMT  
		Size: 13.1 MB (13141250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d896a8ffbf96431c2e3625e5c0bf80b26d5575151162818bb96feadf987a21b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40454569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc7a6b4a947b78e2024599c7ed9884c9c3dcf7e77d3da0c19bd9593ca6f8ab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:45 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:46 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:50 GMT
ADD file:b85182b4593c262faef116755e01baa608e8090e1cb697d735485ff0bd5b353e in / 
# Mon, 05 Jun 2023 17:02:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d08ab8ea3b2755ec06aa9ce6972e64da08c79b30281c9416cac92b6aa23a7d8`  
		Last Modified: Fri, 16 Jun 2023 02:34:35 GMT  
		Size: 26.7 MB (26727371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11fa3a4a444d42bc471027a78d4e890bb44584c98f6160625eb80e66f566049`  
		Last Modified: Fri, 16 Jun 2023 02:34:32 GMT  
		Size: 13.7 MB (13727198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:afde62e2338b4677dcd7c066530ac56c757d0c71c72e0b8c465f19b02e31625c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48336324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880f87ce67ddc9c97e45502bb7b7982c49ddaf7e2d64e4ae7308bf8b59a7387`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:48 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:52 GMT
ADD file:48c30fe281554302bb6533dd33a43a0877851ac5ba59dc3aff3d3d9ceae6f8a9 in / 
# Mon, 05 Jun 2023 17:10:52 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:04:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e97b48410348d002f0aaa3d5e7df14543cadcf78a962c446f311040094d1348`  
		Last Modified: Fri, 16 Jun 2023 01:27:17 GMT  
		Size: 32.1 MB (32102208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf4d9ebe87a9f4a30cb3454f9146c64bf5f745c3afc33b5ef9066928de29bc3`  
		Last Modified: Fri, 16 Jun 2023 01:27:13 GMT  
		Size: 16.2 MB (16234116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e763b1803ec5c6f89992cc212bddc67f914a766d4ba967e729c1907db7688d55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40379050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a913ebcfdf6e18e2d5e646ca355d2234fda1a2ef937cfb34c313b17f5660fb17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:49 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:51 GMT
ADD file:2390e4c5ac4f862cf5fb266c70962a01f271fa692b74af886f18911482025825 in / 
# Mon, 05 Jun 2023 17:10:51 GMT
CMD ["/bin/bash"]
# Sat, 17 Jun 2023 09:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45d37589c642f2585803ed2ba24d2b897920c885c7a913bb399e12a2410d5503`  
		Last Modified: Sat, 17 Jun 2023 10:01:25 GMT  
		Size: 26.0 MB (26034488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10ce8336984e795efd05d14a13611a92ef77b199d749859036bd37fbbf18040`  
		Last Modified: Sat, 17 Jun 2023 10:01:24 GMT  
		Size: 14.3 MB (14344562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
