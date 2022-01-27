<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-buster-slim`](#rethinkdb2-buster-slim)
-	[`rethinkdb:2-centos`](#rethinkdb2-centos)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-buster-slim`](#rethinkdb24-buster-slim)
-	[`rethinkdb:2.4-centos`](#rethinkdb24-centos)
-	[`rethinkdb:2.4.1`](#rethinkdb241)
-	[`rethinkdb:2.4.1-buster-slim`](#rethinkdb241-buster-slim)
-	[`rethinkdb:2.4.1-centos`](#rethinkdb241-centos)
-	[`rethinkdb:buster-slim`](#rethinkdbbuster-slim)
-	[`rethinkdb:centos`](#rethinkdbcentos)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-buster-slim`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-buster-slim`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.1-centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2.4.1-centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:centos`

```console
$ docker pull rethinkdb@sha256:0dba02987090e751b491d9ebd70890c37690f4eed1b81972f86deea1d7db8c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:centos` - linux; amd64

```console
$ docker pull rethinkdb@sha256:4f8964161ce484c16f65c8c6e206dd758793adf06c53993eac651bdb9c1649ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76992aa3ff22017132fc0d31a6c2cd470a5d8929b7cd7e71356d4421052abf03`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:49:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1
# Wed, 15 Sep 2021 19:49:38 GMT
RUN echo $'[rethinkdb]\nname=RethinkDB\nenabled=1\nbaseurl=https://download.rethinkdb.com/repository/centos/8/x86_64/\ngpgkey=https://download.rethinkdb.com/repository/raw/pubkey.gpg\ngpgcheck=1\n' >> /etc/yum.repos.d/rethinkdb.repo
# Wed, 15 Sep 2021 19:49:48 GMT
RUN yum install -y rethinkdb-$RETHINKDB_PACKAGE_VERSION 	&& yum clean all
# Wed, 15 Sep 2021 19:49:48 GMT
VOLUME [/data]
# Wed, 15 Sep 2021 19:49:49 GMT
WORKDIR /data
# Wed, 15 Sep 2021 19:49:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 15 Sep 2021 19:49:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14535878a922d6f2b6784f3df0b1171a760b89f733accf8864763f80ce565fc`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83765c84b45bb249242f550b991fa45fdc0417c90860657ca7a763a28f23d652`  
		Last Modified: Wed, 15 Sep 2021 19:50:39 GMT  
		Size: 22.4 MB (22426554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a6d0670eea07ae2e798a19685994d7486109329162bdcdbc1da3b739967e`  
		Last Modified: Wed, 15 Sep 2021 19:50:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:cfe1391a8f0abb014b67656c29d5973ef65e02cd26aa2ee5591ed4b392167214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:68ed28ebd8e5fe294de8b5bde41827a4198d1274ad959c024ddf60013d250faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcde62cc368fb17a15904c56de540db665b7f25cded2dcf0f3279930144bc58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:50:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:27 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 26 Jan 2022 22:51:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 26 Jan 2022 22:51:39 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 22:51:40 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:51:40 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:51:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 26 Jan 2022 22:51:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc159111b2a221d43660a880281487f17be064d9aef081b89ad5160d517efe1`  
		Last Modified: Wed, 26 Jan 2022 22:52:09 GMT  
		Size: 6.7 MB (6691276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b12a3865bbe5d562d252c688e1299a6b1586ee2606218bf55df8ea8af6662f9`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 2.6 KB (2613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5124e5f11f05cdca313a87be3362e9da4749616dc72b339bebc3d36a7bca2af`  
		Last Modified: Wed, 26 Jan 2022 22:52:11 GMT  
		Size: 18.0 MB (17991494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb56a01927174ee76318cb2bc453fd9f3244d22bb42035f87e88bf7fbdc593`  
		Last Modified: Wed, 26 Jan 2022 22:52:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
