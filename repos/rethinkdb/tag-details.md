<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2.4.0`](#rethinkdb240)
-	[`rethinkdb:2.4.0-buster-slim`](#rethinkdb240-buster-slim)
-	[`rethinkdb:2.4.0-centos`](#rethinkdb240-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:4d8fd53396f652c32467befbe0c1b02e1c43abd9db4b318d292a11812fe977fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:f71dbfadd8b89d1f62425b19f5704b8de42930748d095c18ac2605a7f38fe4ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51786968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15528906809b33953c7a803eafb6f093c47e5d0468d3d37736a0345907fa2524`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:06:36 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Fri, 12 Mar 2021 22:06:45 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:46 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:46 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:46 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:46 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d394513eae3bce3dd61659e6b9394d699355c0b06cc083ba4f92f3fa853e97ab`  
		Last Modified: Fri, 12 Mar 2021 22:08:13 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0019c345489bacb6215b8135522ed0d025ce7dda81df9f8a61b53cee59c4a7eb`  
		Last Modified: Fri, 12 Mar 2021 22:08:17 GMT  
		Size: 18.0 MB (17992923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0764d7dbd6dadab1d55e03068b0fa6f1e1c4b4e1f280f9a6febc7e2d58e66469`  
		Last Modified: Fri, 12 Mar 2021 22:08:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:4d8fd53396f652c32467befbe0c1b02e1c43abd9db4b318d292a11812fe977fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:f71dbfadd8b89d1f62425b19f5704b8de42930748d095c18ac2605a7f38fe4ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51786968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15528906809b33953c7a803eafb6f093c47e5d0468d3d37736a0345907fa2524`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:06:36 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Fri, 12 Mar 2021 22:06:45 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:46 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:46 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:46 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:46 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d394513eae3bce3dd61659e6b9394d699355c0b06cc083ba4f92f3fa853e97ab`  
		Last Modified: Fri, 12 Mar 2021 22:08:13 GMT  
		Size: 2.6 KB (2618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0019c345489bacb6215b8135522ed0d025ce7dda81df9f8a61b53cee59c4a7eb`  
		Last Modified: Fri, 12 Mar 2021 22:08:17 GMT  
		Size: 18.0 MB (17992923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0764d7dbd6dadab1d55e03068b0fa6f1e1c4b4e1f280f9a6febc7e2d58e66469`  
		Last Modified: Fri, 12 Mar 2021 22:08:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-centos`

```console
$ docker pull rethinkdb@sha256:11d9649e49b7e3b68d5d28e3e3959b055a6f7639bab3bc810e8afe96c6e7cc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:17689662917e7af14d2bebf46cd6890ee8badf9b74e8e8b1480ec0b6bde5a29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f93c64f13e16520ee2f13c350b04b364d79f12de5f07eb0ab11357643807bf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0
# Fri, 12 Mar 2021 22:06:51 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:59 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:59 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:07:00 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:07:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:07:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25076e20c46678ae755ba6afa36d6d81841dc318bbf67e12e1dc65a61830d747`  
		Last Modified: Fri, 12 Mar 2021 22:08:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a6c1b31a4042d1cd7786c6f48d8c3d4f0c4694af26eef0a12a818bfb31e040`  
		Last Modified: Fri, 12 Mar 2021 22:08:32 GMT  
		Size: 22.3 MB (22329806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b305cc56442aaa917ad4c80c57d1d01db071a009e92c3a8f5129445a25b4eb`  
		Last Modified: Fri, 12 Mar 2021 22:08:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:b64ea5554c79140250dcb1b9890a403d81dda0562b8b747a9f8f03507fafa6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:19543b769d6fc6364ebf7e49586a5393f1e4aea8c846b1b66becd6309be84b9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c64b1fd4d8d7be12e58683646b567a9b21e435a629175801f20ace09eed40b0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Mar 2021 22:06:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Fri, 12 Mar 2021 22:06:11 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Fri, 12 Mar 2021 22:06:23 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Fri, 12 Mar 2021 22:06:23 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:24 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e6677aefac3d9eae873c0dcf112163e1d7c02e8b1c6440876d95a5fa448d`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308bfa96e4023aefc38b6afabf4bab16585c81dca08a9846cf82a86d1ab02186`  
		Last Modified: Fri, 12 Mar 2021 22:07:56 GMT  
		Size: 22.3 MB (22329396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c75a151438cb5b472c183e238e3ce14e21bbab2ba06c6ca56bc5bffc489866`  
		Last Modified: Fri, 12 Mar 2021 22:07:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:2a8b0eab9c74521a6a91955fe64709a50eb3190e80b053085aad59e2da5aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:73d44a95fd9fe0fa6189531cb29ffc5c27b44e7eb1cafe7c9efe346410983220
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277a57c45c1b1e06389c24c145d266edb4076c553011b5b67eee1f7e3664513`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 22:05:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:05:49 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 12 Mar 2021 22:05:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 12 Mar 2021 22:06:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 22:06:00 GMT
VOLUME [/data]
# Fri, 12 Mar 2021 22:06:01 GMT
WORKDIR /data
# Fri, 12 Mar 2021 22:06:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 12 Mar 2021 22:06:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8377f19a6a09f38d41be63c39185e22a7073adf2cc19ad8e7bb69ec9ea152d39`  
		Last Modified: Fri, 12 Mar 2021 22:07:23 GMT  
		Size: 6.7 MB (6690301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63df49fcb4ffb8767c2d6b3603b389e14fd3dfd47ee56b75cdd2d14c1e95880b`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d202fbc8eeeb7667d1b86bb79443f049c27aab5e038e66aea838399901cbe`  
		Last Modified: Fri, 12 Mar 2021 22:07:25 GMT  
		Size: 18.0 MB (17991880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf2bc977bc6225b9abb578f45276553e2464b20883bd14b28b4b0f1e8f2473c`  
		Last Modified: Fri, 12 Mar 2021 22:07:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
