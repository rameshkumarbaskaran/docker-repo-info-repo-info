<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bullseye-slim`](#rethinkdb2-bullseye-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bullseye-slim`](#rethinkdb24-bullseye-slim)
-	[`rethinkdb:2.4.2`](#rethinkdb242)
-	[`rethinkdb:2.4.2-bullseye-slim`](#rethinkdb242-bullseye-slim)
-	[`rethinkdb:bullseye-slim`](#rethinkdbbullseye-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:92e0a6a1fcf7be37cae38a274002d6c9f2372c3ce2cf5a136f7ccf5c8dfd75ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88342bf62ee52b14e3aacd16cd0836248d72be34df78bc7510d97a3ff50152d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45737528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d1b48df760e17172198b76562bf7892eb7c008e03e8619f0d6d9ea70062ff0`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:54:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:54:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:54:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:54:49 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:54:50 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:54:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:54:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb798efcdcaae74f91bcb0ace60426a35282030913bf7275c3deca829dffaaa`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 6.3 MB (6308354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf5428c08948c61a4e31a351f288b3c521e35ff08c841b2c366d6d532769e70`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37601cf141f7fabbd2762548457a870c51364e5e3fc245e992f820ef90ecc`  
		Last Modified: Tue, 13 Sep 2022 12:55:18 GMT  
		Size: 9.4 MB (9372172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f90a8ee3ced5331433eb37004438abfdfcf41fd0bbad320481c56aabf909c`  
		Last Modified: Tue, 13 Sep 2022 12:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:3fa83f5d08d58b4c8fe160235ebb90669e28a2449eaf0efb67297ede804a4d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45431537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040ed421c217d3d47ae79aa5363e15f48b9ff442f56b7405b9da26b9f2a8ddb8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:02:28 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 05 Oct 2022 03:02:30 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 05 Oct 2022 03:02:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:02:36 GMT
VOLUME [/data]
# Wed, 05 Oct 2022 03:02:36 GMT
WORKDIR /data
# Wed, 05 Oct 2022 03:02:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 05 Oct 2022 03:02:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844052b0e573d959a29635a4e114263dc81d516b25fcf80581d7780425f06f`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 6.2 MB (6205607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ea1a131080425a363ecdfbf94864ab4f989718bc2171110c018b35ad6d0b3`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d8be98bc28b967cb27671647323e71a8eaee486bf5193f57f1037712ca583`  
		Last Modified: Wed, 05 Oct 2022 03:03:05 GMT  
		Size: 9.6 MB (9572402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f595e22b8386d30f0fada7cb45d01604bbee26d9d5316a4773e52a672a6bb84`  
		Last Modified: Wed, 05 Oct 2022 03:03:04 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
