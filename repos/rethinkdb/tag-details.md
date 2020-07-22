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
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0`

```console
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.0-buster-slim`

```console
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4.0-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
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
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.4-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
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
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
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
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
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
$ docker pull rethinkdb@sha256:4cb806ed8ba198cb70d0a5e78f3e41f624b59c0e5d253a74a8dfa7af12a94909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1302f285ed41addece3b0599edebaa9cfa599142a42efe668dc963a1779fa0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576fb9c543d23ed2e827adb5372f198005bf30e751c1abbc54466e397c60ac1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:27:37 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:39 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 22 Jul 2020 20:27:39 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Wed, 22 Jul 2020 20:27:51 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:27:51 GMT
VOLUME [/data]
# Wed, 22 Jul 2020 20:27:51 GMT
WORKDIR /data
# Wed, 22 Jul 2020 20:27:52 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Jul 2020 20:27:52 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a22f4d21c0c2d85823c1edd01fbb7c017e11b89ddc4d99f92c0f14a5a617e`  
		Last Modified: Wed, 22 Jul 2020 20:28:15 GMT  
		Size: 6.7 MB (6669148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8303b6174c2124b29a0384d0b7d7c2289ee77a9b8eba890fd2d301d23848fa40`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736c451157e79f2ce330864bc43ffda0c28800686141553ae2825256b70219e`  
		Last Modified: Wed, 22 Jul 2020 20:28:17 GMT  
		Size: 18.0 MB (17992065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cba450f2c153f85b4424ed8c915e87b09599770e28e011719f1bbfe8f972d`  
		Last Modified: Wed, 22 Jul 2020 20:28:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
