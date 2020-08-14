<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:5d0f079607ae53358c87cc3be88b2d897e16489ee4300889614575a591d4b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e589a337584afcbe4858aff85c4275bd3d985e8e561245bafb52f3fa00a4872d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3769bad6ed271504117db2e120e7efd0e4b2bb5038a268c20e03f84f0f03b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 10 Aug 2020 19:00:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Mon, 10 Aug 2020 19:00:15 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 10 Aug 2020 19:00:16 GMT
VOLUME [/data]
# Mon, 10 Aug 2020 19:00:16 GMT
WORKDIR /data
# Mon, 10 Aug 2020 19:00:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 10 Aug 2020 19:00:16 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb87697a5f6eecce6450ac019a8130a4ea44c119422b89a275b80895068a83`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae708913553e0f013132c8c4ed53e5e35056d12d0faac39d16abb4626f78efc`  
		Last Modified: Mon, 10 Aug 2020 19:00:56 GMT  
		Size: 18.0 MB (17992176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3829cbfee612b0dc16f078822928b048d0e38c716cbfd5853134214bd51d07`  
		Last Modified: Mon, 10 Aug 2020 19:00:53 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:115347ac348bbd0c47964b9d4752eee50a939ef89800bfa8c913b57155c84bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b75b236e0d67b1d8c7f7d3800179cabd1ec330719a7d51c9155fce82fd4231eb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97239408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4c32f9f785547d2206f4d058e96229d571c31d6a714d32570dbf672ce015ed`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 19:00:22 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Mon, 10 Aug 2020 19:00:23 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:36 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:36 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:37 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692940a286c0d3f1beadabb7a212a6e1678d9c0e303ac94a5bf35eb3734cadb2`  
		Last Modified: Fri, 14 Aug 2020 21:14:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ff4bec25e8a9c3995aa160e716057e6833426bc14c40925c0c9153efa3758`  
		Last Modified: Fri, 14 Aug 2020 21:14:29 GMT  
		Size: 22.4 MB (22370928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be9a2117906713867ccadcfe5b95b109d1b8f5788bb2fed8736ddcae099972b`  
		Last Modified: Fri, 14 Aug 2020 21:14:24 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:ff373e004421806fce99fb671c77cc5501f94033e7b71e098217b06527a6c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1657b2cdf8aa6349ee420f6dd13742464a5f10f6c9afa7452f21bc77dadb6680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc67788580c45d661eca9eee275f454bad6b9f39847268008a4d3b32f6e5c7e6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Aug 2020 21:12:58 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 14 Aug 2020 21:12:59 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 14 Aug 2020 21:13:11 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 14 Aug 2020 21:13:12 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:13:12 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:13:12 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:13:13 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab244016302f983bd67f48b1617ff02399bff6c698eb9fbe14e9fb697cce3d27`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afcadaf6949665a0a4e3476e4aea8716dfe440805296483f5d251343e3b7aad`  
		Last Modified: Fri, 14 Aug 2020 21:14:18 GMT  
		Size: 22.4 MB (22373453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5e734cc4ca195caee21f22078178255473a5f345528d5bf12d82d2fb8b1e0`  
		Last Modified: Fri, 14 Aug 2020 21:14:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
