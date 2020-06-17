<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:97945571d761d1c6d13ed1c5b19c431829a165eae8979e95a43146244044296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:62b8895efb80423198ab0f72f481d21cbd46359abc1486702be4ba1d56a25a7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97244258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e1670ba60391d24a97d5a7b3e70a9c18ecb8683cd690ebe8ca6ec2898591b3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Jun 2020 00:22:24 GMT
ADD file:84700c11fcc969ac08ef25f115513d76c7b72a4118c01fbc86ef0a6056fdebeb in / 
# Wed, 17 Jun 2020 00:22:25 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200611
# Wed, 17 Jun 2020 00:22:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 00:45:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Wed, 17 Jun 2020 00:45:00 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 17 Jun 2020 00:45:12 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 17 Jun 2020 00:45:12 GMT
VOLUME [/data]
# Wed, 17 Jun 2020 00:45:12 GMT
WORKDIR /data
# Wed, 17 Jun 2020 00:45:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Jun 2020 00:45:12 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6910e5a164f725142d77994b247ba20040477fbab49a721bdbe8d61cf855ac23`  
		Last Modified: Wed, 17 Jun 2020 00:23:52 GMT  
		Size: 74.9 MB (74866818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d202930a85138a93b068d1eccecb1b05af9be3ebf00c897408f75ca8e1d94d`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c34589253a77f1123f119cd191e186943036825f376131178d3e138511acb0`  
		Last Modified: Wed, 17 Jun 2020 00:45:35 GMT  
		Size: 22.4 MB (22377081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc88e46cf376b3042a553f6853b4d0d091ef6fb76fef0d1d9d64ffec7da7a81`  
		Last Modified: Wed, 17 Jun 2020 00:45:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
