<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.7`](#varnish607)
-	[`varnish:6.0.7-1`](#varnish607-1)
-	[`varnish:6.6`](#varnish66)
-	[`varnish:6.6.0`](#varnish660)
-	[`varnish:6.6.0-1`](#varnish660-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:c90b921f5a39ed8e27c77b0a5dc10e0d4e95bbfa8d1953c453d642033a5c8c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:8ac30b2bf74c08c4a3a12f804d64d12199333417df63c5af2b39c16eafa7a5f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029061c774bf6378b511bf2b994cc8693841d0a2eb831526c1200c4dec405d03`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:03 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:03 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:04 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387be2f59b98db43ba6e89745e00820b60faaade6ad68293b9170c05e3047943`  
		Last Modified: Sat, 10 Apr 2021 18:28:50 GMT  
		Size: 798.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7`

```console
$ docker pull varnish@sha256:c90b921f5a39ed8e27c77b0a5dc10e0d4e95bbfa8d1953c453d642033a5c8c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7` - linux; amd64

```console
$ docker pull varnish@sha256:8ac30b2bf74c08c4a3a12f804d64d12199333417df63c5af2b39c16eafa7a5f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029061c774bf6378b511bf2b994cc8693841d0a2eb831526c1200c4dec405d03`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:03 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:03 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:04 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387be2f59b98db43ba6e89745e00820b60faaade6ad68293b9170c05e3047943`  
		Last Modified: Sat, 10 Apr 2021 18:28:50 GMT  
		Size: 798.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7-1`

```console
$ docker pull varnish@sha256:c90b921f5a39ed8e27c77b0a5dc10e0d4e95bbfa8d1953c453d642033a5c8c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7-1` - linux; amd64

```console
$ docker pull varnish@sha256:8ac30b2bf74c08c4a3a12f804d64d12199333417df63c5af2b39c16eafa7a5f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029061c774bf6378b511bf2b994cc8693841d0a2eb831526c1200c4dec405d03`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:03 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:03 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:04 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387be2f59b98db43ba6e89745e00820b60faaade6ad68293b9170c05e3047943`  
		Last Modified: Sat, 10 Apr 2021 18:28:50 GMT  
		Size: 798.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0-1`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:cd01701adbc3cab85bdd30272f349dbf4eecd8074dcf1b7abc5951b41e3a108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:93c252822a0fb7af536ed4b9bf99b887c128ff499035f5dd1843ecff784c7779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea141d9d469c46905d72c97bfe0196fd4acd7413a5a87df5eb232e692f85a6ed`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:31 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:31 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:31 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde437595c75381edf46cec0f22f9bee9f5f45c4fb22d9b17828398ab06ba5ee`  
		Last Modified: Sat, 10 Apr 2021 18:29:13 GMT  
		Size: 797.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:c90b921f5a39ed8e27c77b0a5dc10e0d4e95bbfa8d1953c453d642033a5c8c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:8ac30b2bf74c08c4a3a12f804d64d12199333417df63c5af2b39c16eafa7a5f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029061c774bf6378b511bf2b994cc8693841d0a2eb831526c1200c4dec405d03`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Sat, 10 Apr 2021 18:28:03 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Sat, 10 Apr 2021 18:28:03 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 10 Apr 2021 18:28:04 GMT
EXPOSE 80 8443
# Sat, 10 Apr 2021 18:28:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387be2f59b98db43ba6e89745e00820b60faaade6ad68293b9170c05e3047943`  
		Last Modified: Sat, 10 Apr 2021 18:28:50 GMT  
		Size: 798.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
