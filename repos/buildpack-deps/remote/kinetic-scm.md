## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:79b0e2824c5decff024b71255f2f167db0b151a2ce23502a119f0a6dc0d17cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d52ddd72ddd4f630e64370ad14d0ec6b99705784fc76f396c2d3d67230db3403
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81504021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec8c6e4d643fed5a6197bd272d12574893b6727b71d0bddc0526d40019fb457`
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
# Tue, 04 Jul 2023 03:44:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7e60069d839c80c438523487b52eb9073ef4a8fd32af5b8a6dfe8480792c8a57`  
		Last Modified: Tue, 04 Jul 2023 03:57:02 GMT  
		Size: 39.8 MB (39825912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:191786f742e3c3287b0bc0d2eb4a014322bd27ea0399bb107b1022dfdff7241e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81994985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61c2cf6d18409c5f049992d0a00aec601ded1ab9fb76d5c1c5f6ce49feb4f9c`
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
# Fri, 16 Jun 2023 00:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9f1ff3680907d768021e43095ea76751da3011e63414be63b980806f2ce05d85`  
		Last Modified: Fri, 16 Jun 2023 00:59:12 GMT  
		Size: 42.9 MB (42939688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:82f1fe853fc8a21e8b4cd523a76bfc328c0824c2952152203f0fe254397379ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80090558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534cedcae680c182fe39dcaba296532a086079521aae79d3de3d289c291d5dc7`
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
# Fri, 16 Jun 2023 02:21:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b51bbb1bce4e9d99daf88e47964d3e6228a1af3e8c83e9aa282d385788830cfa`  
		Last Modified: Fri, 16 Jun 2023 02:34:48 GMT  
		Size: 39.6 MB (39635989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:264fc69c8de3193a7191aae5bb3f4c3db4fbf1a9f0e72d801c70971713aadbda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92568101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6367bde1dbdeeadc100e3b50d95455d079ffc7c8f892d24e31742464e7e00931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4c2a73576db8e1d5b385d67fe412db5e6cd146167f6c5fa6153b87f17abfc3d`  
		Last Modified: Tue, 04 Jul 2023 04:44:10 GMT  
		Size: 32.1 MB (32102426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297facc34b9d65726d36999c1b9378836014f1dbb15725b2be4359b50bec9d21`  
		Last Modified: Tue, 04 Jul 2023 04:44:07 GMT  
		Size: 16.2 MB (16234063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb9fc38b5a1da1252223c33aa1381def6fb94284f39b6c1d6025d92bf99478`  
		Last Modified: Tue, 04 Jul 2023 04:44:34 GMT  
		Size: 44.2 MB (44231612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:749616a3d80ce076f174efe52ab324d25a6fb91799a0be44c3b5ec95d468e9df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80057057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e27248efe9b740d475c4c4dce3899539f672e413e71005bf1c2b8ce39fe9eb0`
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
# Sat, 17 Jun 2023 09:50:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:15f89ec5257613dfb7e6ac3731cf008ae93397126d7d27b80d7d9e63428331cd`  
		Last Modified: Sat, 17 Jun 2023 10:01:38 GMT  
		Size: 39.7 MB (39678007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
