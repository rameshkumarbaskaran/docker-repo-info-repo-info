<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `thrift`

-	[`thrift:0.10`](#thrift010)
-	[`thrift:0.10.0`](#thrift0100)
-	[`thrift:0.11`](#thrift011)
-	[`thrift:0.11.0`](#thrift0110)
-	[`thrift:0.12`](#thrift012)
-	[`thrift:0.12.0`](#thrift0120)
-	[`thrift:0.9`](#thrift09)
-	[`thrift:0.9.3`](#thrift093)
-	[`thrift:latest`](#thriftlatest)

## `thrift:0.10`

```console
$ docker pull thrift@sha256:d64f9113aa9e9f2aef76d549706a7225582fb67d5135011291ee61b9d2b80549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.10` - linux; amd64

```console
$ docker pull thrift@sha256:5f8469a3150c764d0c309f0b24a908c01b76ecb81c103610959c77f905b8f0ca
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52326768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8b1ba2ebbc896ea256be716e43d46b4e37b4014e5c6f190b450086416f7331`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:53:16 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 05 Mar 2019 05:53:16 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 05 Mar 2019 05:56:18 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:56:19 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad12300e9f30c98611be0415a2462ed13e458009514beb94e95c1346455ac3`  
		Last Modified: Tue, 05 Mar 2019 06:00:08 GMT  
		Size: 13.0 MB (12986993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.10.0`

```console
$ docker pull thrift@sha256:d64f9113aa9e9f2aef76d549706a7225582fb67d5135011291ee61b9d2b80549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.10.0` - linux; amd64

```console
$ docker pull thrift@sha256:5f8469a3150c764d0c309f0b24a908c01b76ecb81c103610959c77f905b8f0ca
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52326768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8b1ba2ebbc896ea256be716e43d46b4e37b4014e5c6f190b450086416f7331`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:53:16 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 05 Mar 2019 05:53:16 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 05 Mar 2019 05:56:18 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:56:19 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad12300e9f30c98611be0415a2462ed13e458009514beb94e95c1346455ac3`  
		Last Modified: Tue, 05 Mar 2019 06:00:08 GMT  
		Size: 13.0 MB (12986993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.11`

```console
$ docker pull thrift@sha256:91f11a3b96b5dff6777206e851b12ec22493cf3d1ecc395817da15b204912b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.11` - linux; amd64

```console
$ docker pull thrift@sha256:e27dcf3ecc33c21e2e8dc61a6d73ef389a01f2d7ba9d7ab61126335c507e3874
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52472410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1086389f2e1311402e9b398489f113409dffc4bad675370ab45e352cfc379cc`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:56:30 GMT
LABEL authors=Adam Hawkins <hi@ahawkins.me>
# Tue, 05 Mar 2019 05:56:31 GMT
ENV THRIFT_VERSION=0.11.0
# Tue, 05 Mar 2019 05:59:36 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:59:36 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fd9411bafd139f0ebe70fd4dc46a0c57c5c1d659f5763230091e9d4857c514`  
		Last Modified: Tue, 05 Mar 2019 06:00:17 GMT  
		Size: 13.1 MB (13132635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.11.0`

```console
$ docker pull thrift@sha256:91f11a3b96b5dff6777206e851b12ec22493cf3d1ecc395817da15b204912b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.11.0` - linux; amd64

```console
$ docker pull thrift@sha256:e27dcf3ecc33c21e2e8dc61a6d73ef389a01f2d7ba9d7ab61126335c507e3874
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52472410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1086389f2e1311402e9b398489f113409dffc4bad675370ab45e352cfc379cc`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:56:30 GMT
LABEL authors=Adam Hawkins <hi@ahawkins.me>
# Tue, 05 Mar 2019 05:56:31 GMT
ENV THRIFT_VERSION=0.11.0
# Tue, 05 Mar 2019 05:59:36 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:59:36 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fd9411bafd139f0ebe70fd4dc46a0c57c5c1d659f5763230091e9d4857c514`  
		Last Modified: Tue, 05 Mar 2019 06:00:17 GMT  
		Size: 13.1 MB (13132635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.12`

```console
$ docker pull thrift@sha256:7cb2f20b73e2459e4ddb29261d2ac7d4919b57ce7af6bc9070391ac467de8177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.12` - linux; amd64

```console
$ docker pull thrift@sha256:3c5976c992de963f421ec5e3b914a6e68ec7ae3fa5df942f9abf2bd7b32a5ad8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43743109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafa2d18f771f1554a69470b8075be1ddb2c767f65c6315869e463548a4dd24`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 03:28:55 GMT
ENV THRIFT_VERSION=v0.12.0
# Wed, 14 Jul 2021 03:32:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -k -sSL "https://github.com/apache/thrift/archive/${THRIFT_VERSION}.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./bootstrap.sh 	&& ./configure --disable-libs 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/cache/apt/* 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/* 	&& rm -rf /var/tmp/*
# Wed, 14 Jul 2021 03:32:56 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad653376105cd82823d8bce467c8af3844d4f7204bc6ec2b451eddeafa523c`  
		Last Modified: Wed, 14 Jul 2021 03:33:18 GMT  
		Size: 17.0 MB (17036964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.12.0`

```console
$ docker pull thrift@sha256:7cb2f20b73e2459e4ddb29261d2ac7d4919b57ce7af6bc9070391ac467de8177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.12.0` - linux; amd64

```console
$ docker pull thrift@sha256:3c5976c992de963f421ec5e3b914a6e68ec7ae3fa5df942f9abf2bd7b32a5ad8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43743109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafa2d18f771f1554a69470b8075be1ddb2c767f65c6315869e463548a4dd24`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 03:28:55 GMT
ENV THRIFT_VERSION=v0.12.0
# Wed, 14 Jul 2021 03:32:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -k -sSL "https://github.com/apache/thrift/archive/${THRIFT_VERSION}.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./bootstrap.sh 	&& ./configure --disable-libs 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/cache/apt/* 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/* 	&& rm -rf /var/tmp/*
# Wed, 14 Jul 2021 03:32:56 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad653376105cd82823d8bce467c8af3844d4f7204bc6ec2b451eddeafa523c`  
		Last Modified: Wed, 14 Jul 2021 03:33:18 GMT  
		Size: 17.0 MB (17036964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9`

```console
$ docker pull thrift@sha256:965273845365074a76e03c28b6864dae3095db3d5391ec6165f20285eb71848b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.9` - linux; amd64

```console
$ docker pull thrift@sha256:c43b53fad1de73bf35ee49f8f467086714c4ea0196cb5736aca6e06c3377166d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51268919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e12c5473f809a9b51e884fa4d561f38cd7bf0d6a292e2b86235fb6d067fceb0`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:50:17 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Tue, 05 Mar 2019 05:50:17 GMT
ENV THRIFT_VERSION=0.9.3
# Tue, 05 Mar 2019 05:53:08 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:53:08 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6041c79e2dc6260699d507894183d8c0d62f65123b5cf7e021c9ebf2f15b22`  
		Last Modified: Tue, 05 Mar 2019 06:00:00 GMT  
		Size: 11.9 MB (11929144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9.3`

```console
$ docker pull thrift@sha256:965273845365074a76e03c28b6864dae3095db3d5391ec6165f20285eb71848b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:0.9.3` - linux; amd64

```console
$ docker pull thrift@sha256:c43b53fad1de73bf35ee49f8f467086714c4ea0196cb5736aca6e06c3377166d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51268919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e12c5473f809a9b51e884fa4d561f38cd7bf0d6a292e2b86235fb6d067fceb0`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 04 Mar 2019 23:23:13 GMT
ADD file:bbbee952d330957b2a425a378d451176c784585717c9e47df6c05c10881a7b3c in / 
# Mon, 04 Mar 2019 23:23:13 GMT
CMD ["bash"]
# Tue, 05 Mar 2019 05:50:17 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Tue, 05 Mar 2019 05:50:17 GMT
ENV THRIFT_VERSION=0.9.3
# Tue, 05 Mar 2019 05:53:08 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 05 Mar 2019 05:53:08 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:2b15b7abe8b39a409a8b29c5ce62b22ce091102ca25fbf49aa877cca40983717`  
		Last Modified: Mon, 04 Mar 2019 23:27:27 GMT  
		Size: 39.3 MB (39339775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6041c79e2dc6260699d507894183d8c0d62f65123b5cf7e021c9ebf2f15b22`  
		Last Modified: Tue, 05 Mar 2019 06:00:00 GMT  
		Size: 11.9 MB (11929144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:latest`

```console
$ docker pull thrift@sha256:7cb2f20b73e2459e4ddb29261d2ac7d4919b57ce7af6bc9070391ac467de8177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `thrift:latest` - linux; amd64

```console
$ docker pull thrift@sha256:3c5976c992de963f421ec5e3b914a6e68ec7ae3fa5df942f9abf2bd7b32a5ad8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43743109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aafa2d18f771f1554a69470b8075be1ddb2c767f65c6315869e463548a4dd24`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 03:28:55 GMT
ENV THRIFT_VERSION=v0.12.0
# Wed, 14 Jul 2021 03:32:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -k -sSL "https://github.com/apache/thrift/archive/${THRIFT_VERSION}.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./bootstrap.sh 	&& ./configure --disable-libs 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/cache/apt/* 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/* 	&& rm -rf /var/tmp/*
# Wed, 14 Jul 2021 03:32:56 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad653376105cd82823d8bce467c8af3844d4f7204bc6ec2b451eddeafa523c`  
		Last Modified: Wed, 14 Jul 2021 03:33:18 GMT  
		Size: 17.0 MB (17036964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
