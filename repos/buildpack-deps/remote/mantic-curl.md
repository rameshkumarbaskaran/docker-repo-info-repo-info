## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:908d0be713935fbd7d3acb60f068f596d148edb9e567546d8b91a8be63550951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:19eadafd7e47f80e366378c5051926be8052c9cecb54f1fcd52d56a34cf7265f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40377459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e13ee1c076a497e405e37c64f1893d90d7c0245fddc7112d9871559f141b78b`
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

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:19c5ed268e2b8e524d946a28ed2f319b5e25c1f1adfa427b6bb5b30f05219a46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc588db3883f18458453f2ee1e8c9eb7ff1c3a35bd1d10895da7ee6474a7032`
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
