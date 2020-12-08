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
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:050f2b26eb24fbf7ffedb03729f129bb69017d5914225234b1aad92794fc4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:116efebe920037a490e59edad8f0c0a9631449905587ed6c527a201875993dea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34aba053e7c6bb15302f412b9775fd1427f3783a372f6624bfc7254acf2f437`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:23:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:23:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 18 Nov 2020 12:23:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:23:18 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:23:19 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:23:19 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:23:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09288e1a9e2d051d96ce5861c59a8c00e5627e1f8db8d62752cf5788600af284`  
		Last Modified: Wed, 18 Nov 2020 12:24:03 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79682743e7e2ce6c87a2198b22608f58c7cd1e194e8c77599dbfabcc69b387ab`  
		Last Modified: Wed, 18 Nov 2020 12:24:06 GMT  
		Size: 18.0 MB (17992108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7fcee731c9ac6895659e6e080dfe464a8c6eda260c76bb5cc39e7d519e4231`  
		Last Modified: Wed, 18 Nov 2020 12:24:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:050f2b26eb24fbf7ffedb03729f129bb69017d5914225234b1aad92794fc4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:116efebe920037a490e59edad8f0c0a9631449905587ed6c527a201875993dea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34aba053e7c6bb15302f412b9775fd1427f3783a372f6624bfc7254acf2f437`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:23:05 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:23:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 18 Nov 2020 12:23:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:23:18 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:23:19 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:23:19 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:23:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09288e1a9e2d051d96ce5861c59a8c00e5627e1f8db8d62752cf5788600af284`  
		Last Modified: Wed, 18 Nov 2020 12:24:03 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79682743e7e2ce6c87a2198b22608f58c7cd1e194e8c77599dbfabcc69b387ab`  
		Last Modified: Wed, 18 Nov 2020 12:24:06 GMT  
		Size: 18.0 MB (17992108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7fcee731c9ac6895659e6e080dfe464a8c6eda260c76bb5cc39e7d519e4231`  
		Last Modified: Wed, 18 Nov 2020 12:24:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:7c38966f6109abc28bf7d6a760f61738b3700ff909ae29f3fcdcdb9ebd901bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:ce5736a722cb1b0fd0d6b79921cbc40e4a5cb81d12c3f1b3b95e067abfae50c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb51549074acf5d2f9fea2523c6679c9e3b0c0338a5daa404b9d3f65d588b8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:56:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Tue, 08 Dec 2020 00:56:13 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Tue, 08 Dec 2020 00:56:22 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Tue, 08 Dec 2020 00:56:22 GMT
VOLUME [/data]
# Tue, 08 Dec 2020 00:56:23 GMT
WORKDIR /data
# Tue, 08 Dec 2020 00:56:23 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 08 Dec 2020 00:56:23 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f040b4714648b6f92a7ee925071efaef18aba5be86b9caed7d53946866eb9598`  
		Last Modified: Tue, 08 Dec 2020 00:56:50 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4455d10560e81b3e86bef5719a82016dea5f5188d72b93dd3ddeb68aa93412fe`  
		Last Modified: Tue, 08 Dec 2020 00:56:54 GMT  
		Size: 22.3 MB (22330013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fe62d29608f5241c3782f3eda19fbdbf98d2e3da5d762b11155384799d1e38`  
		Last Modified: Tue, 08 Dec 2020 00:56:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:675a7224e465eccf67748eb9747bf0a44c00e53ab1a9764cd57d1d650c6b7209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a9ab5edeaa46c3b0cf02bdf15f5d9503c510bad64ade43b9487911612086c635
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb58d00fcf7cc3361f0035e54d47062c0ce389f12ad5e44b81134e9152e0aab`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:55:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Tue, 08 Dec 2020 00:55:53 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Tue, 08 Dec 2020 00:56:03 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Tue, 08 Dec 2020 00:56:03 GMT
VOLUME [/data]
# Tue, 08 Dec 2020 00:56:03 GMT
WORKDIR /data
# Tue, 08 Dec 2020 00:56:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 08 Dec 2020 00:56:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec050a263eb1b536df655a3f4d2382bd757fe1c35f03b832d7d0ba2e7dfa7cfa`  
		Last Modified: Tue, 08 Dec 2020 00:56:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79bd86fa34f79229b182548217853bb74036f4923de9f2d0aa40c56f3978542`  
		Last Modified: Tue, 08 Dec 2020 00:56:43 GMT  
		Size: 22.3 MB (22329404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37c9f29738a7bfc5fe4dcd5cdb902c80495514ea9e8f43c8cf1b264315b090f`  
		Last Modified: Tue, 08 Dec 2020 00:56:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:675a7224e465eccf67748eb9747bf0a44c00e53ab1a9764cd57d1d650c6b7209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a9ab5edeaa46c3b0cf02bdf15f5d9503c510bad64ade43b9487911612086c635
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb58d00fcf7cc3361f0035e54d47062c0ce389f12ad5e44b81134e9152e0aab`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:55:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Tue, 08 Dec 2020 00:55:53 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Tue, 08 Dec 2020 00:56:03 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Tue, 08 Dec 2020 00:56:03 GMT
VOLUME [/data]
# Tue, 08 Dec 2020 00:56:03 GMT
WORKDIR /data
# Tue, 08 Dec 2020 00:56:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 08 Dec 2020 00:56:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec050a263eb1b536df655a3f4d2382bd757fe1c35f03b832d7d0ba2e7dfa7cfa`  
		Last Modified: Tue, 08 Dec 2020 00:56:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79bd86fa34f79229b182548217853bb74036f4923de9f2d0aa40c56f3978542`  
		Last Modified: Tue, 08 Dec 2020 00:56:43 GMT  
		Size: 22.3 MB (22329404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37c9f29738a7bfc5fe4dcd5cdb902c80495514ea9e8f43c8cf1b264315b090f`  
		Last Modified: Tue, 08 Dec 2020 00:56:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:675a7224e465eccf67748eb9747bf0a44c00e53ab1a9764cd57d1d650c6b7209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a9ab5edeaa46c3b0cf02bdf15f5d9503c510bad64ade43b9487911612086c635
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb58d00fcf7cc3361f0035e54d47062c0ce389f12ad5e44b81134e9152e0aab`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:55:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Tue, 08 Dec 2020 00:55:53 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Tue, 08 Dec 2020 00:56:03 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Tue, 08 Dec 2020 00:56:03 GMT
VOLUME [/data]
# Tue, 08 Dec 2020 00:56:03 GMT
WORKDIR /data
# Tue, 08 Dec 2020 00:56:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 08 Dec 2020 00:56:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec050a263eb1b536df655a3f4d2382bd757fe1c35f03b832d7d0ba2e7dfa7cfa`  
		Last Modified: Tue, 08 Dec 2020 00:56:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79bd86fa34f79229b182548217853bb74036f4923de9f2d0aa40c56f3978542`  
		Last Modified: Tue, 08 Dec 2020 00:56:43 GMT  
		Size: 22.3 MB (22329404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37c9f29738a7bfc5fe4dcd5cdb902c80495514ea9e8f43c8cf1b264315b090f`  
		Last Modified: Tue, 08 Dec 2020 00:56:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:675a7224e465eccf67748eb9747bf0a44c00e53ab1a9764cd57d1d650c6b7209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a9ab5edeaa46c3b0cf02bdf15f5d9503c510bad64ade43b9487911612086c635
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb58d00fcf7cc3361f0035e54d47062c0ce389f12ad5e44b81134e9152e0aab`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Tue, 08 Dec 2020 00:55:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Tue, 08 Dec 2020 00:55:53 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Tue, 08 Dec 2020 00:56:03 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Tue, 08 Dec 2020 00:56:03 GMT
VOLUME [/data]
# Tue, 08 Dec 2020 00:56:03 GMT
WORKDIR /data
# Tue, 08 Dec 2020 00:56:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 08 Dec 2020 00:56:04 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec050a263eb1b536df655a3f4d2382bd757fe1c35f03b832d7d0ba2e7dfa7cfa`  
		Last Modified: Tue, 08 Dec 2020 00:56:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79bd86fa34f79229b182548217853bb74036f4923de9f2d0aa40c56f3978542`  
		Last Modified: Tue, 08 Dec 2020 00:56:43 GMT  
		Size: 22.3 MB (22329404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37c9f29738a7bfc5fe4dcd5cdb902c80495514ea9e8f43c8cf1b264315b090f`  
		Last Modified: Tue, 08 Dec 2020 00:56:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:17401c1edbafb8cc807fdc44016e556de7b686c35d86045fa1a4234b5857281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a5b1c585ce5a5c45ae362bb92f1eea1a653f4326acfce1f76f26231a26722d25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51768068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd5b23cd2539cb34f37912ecc325d0cf53b2a905def5ac15dcb9a4ace4144f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:22:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:34 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 18 Nov 2020 12:22:34 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 18 Nov 2020 12:22:46 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:22:47 GMT
VOLUME [/data]
# Wed, 18 Nov 2020 12:22:47 GMT
WORKDIR /data
# Wed, 18 Nov 2020 12:22:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 18 Nov 2020 12:22:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e447f5e1357f860f3451dcd3ab5cfe3c128cd2fece1ee9a36d64ad1609b4b5c3`  
		Last Modified: Wed, 18 Nov 2020 12:23:49 GMT  
		Size: 6.7 MB (6669182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e01b054557acaca0b77b081da248dd2c131f0976518577554f266a5cdf3cc3`  
		Last Modified: Wed, 18 Nov 2020 12:23:47 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e161d64e52b40a0973d2b765dd9d1fe8e69f825cccbc28eb1b76aed57c764d98`  
		Last Modified: Wed, 18 Nov 2020 12:23:51 GMT  
		Size: 18.0 MB (17990696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a53590d415b928b049c7903ed1b598541c171689418d6b6b775e94c49548d`  
		Last Modified: Wed, 18 Nov 2020 12:23:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
