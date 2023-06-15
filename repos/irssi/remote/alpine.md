## `irssi:alpine`

```console
$ docker pull irssi@sha256:72005f227ec49c5c20c401b0600557ef1093bf5428ac53a33e3da4384cf52b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:3ee61b26e1d47ec3fbeb8f08fde993e9f224a4c1ec0458e29ab857e27d5a2b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18275828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282276d785648e9766e8fd9d8a01fc057024e0eee53bd5c2e00dd9e97a58fe8f`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 21:20:23 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 03 Apr 2023 21:20:24 GMT
ENV HOME=/home/user
# Mon, 03 Apr 2023 21:20:24 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 03 Apr 2023 21:20:24 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 21:20:24 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 03 Apr 2023 21:20:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 03 Apr 2023 21:20:43 GMT
WORKDIR /home/user
# Mon, 03 Apr 2023 21:20:43 GMT
USER user
# Mon, 03 Apr 2023 21:20:43 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975b1b059c5b939df1c482517d4ffc7b023082dda5969abda3d1204119464759`  
		Last Modified: Mon, 03 Apr 2023 21:21:07 GMT  
		Size: 9.7 MB (9730508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237714a25249647b0f0d11a9d1583cd3d59353696fcb9239c152812a03fa9932`  
		Last Modified: Mon, 03 Apr 2023 21:21:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2ca9966d6ff2bff09c5a9cec3577f075d4d9026a11d3b978f730987dee1be1`  
		Last Modified: Mon, 03 Apr 2023 21:21:06 GMT  
		Size: 5.2 MB (5169472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:fafdc2a07b4b1289684f7f7169f227841b158e9b8f10d84de2e41397215dd9b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e75ae9b7b06102652a8a2a145755991c92af8f73710121877f331e2dad4a08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:10:36 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 14 Jun 2023 20:10:36 GMT
ENV HOME=/home/user
# Wed, 14 Jun 2023 20:10:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 14 Jun 2023 20:10:37 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jun 2023 20:10:37 GMT
ENV IRSSI_VERSION=1.4.4
# Wed, 14 Jun 2023 20:10:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 14 Jun 2023 20:10:56 GMT
WORKDIR /home/user
# Wed, 14 Jun 2023 20:10:56 GMT
USER user
# Wed, 14 Jun 2023 20:10:56 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7b983f7d14545bbe51a69bc4446806972c2c3d37196e4533f88a773a4950e1`  
		Last Modified: Wed, 14 Jun 2023 20:11:06 GMT  
		Size: 9.0 MB (9013256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8873c6959849e7492d0a278963eb03b31a0811eea5dd8270be78d7f06ed6fc05`  
		Last Modified: Wed, 14 Jun 2023 20:11:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb55f41f37865c76f3e904400c09f9e958d8b904042fe15598912daf14f17589`  
		Last Modified: Wed, 14 Jun 2023 20:11:05 GMT  
		Size: 5.1 MB (5059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:2abd5d1d07ffa8b59a37f9ba82c93ee387cb798f3c5575e81319b5b483bf3c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16561680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0426aafe3b069e1108b2be2c59139e7eeb36e60c11c057b3e892968e7ce19f`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 21:14:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 03 Apr 2023 21:14:41 GMT
ENV HOME=/home/user
# Mon, 03 Apr 2023 21:14:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 03 Apr 2023 21:14:42 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 21:14:42 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 03 Apr 2023 21:14:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 03 Apr 2023 21:14:58 GMT
WORKDIR /home/user
# Mon, 03 Apr 2023 21:14:58 GMT
USER user
# Mon, 03 Apr 2023 21:14:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbbbe230635515680b7909c4b5725be7b8b5fdd956a1c211e3652857556811d`  
		Last Modified: Mon, 03 Apr 2023 21:15:24 GMT  
		Size: 8.9 MB (8861168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e80a6d0e987fa30151811dbe66899e251b709ace04600da4de7b3b86c3438b1`  
		Last Modified: Mon, 03 Apr 2023 21:15:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c440a0afaa8aef55621b87f0e2fcd598bcfe146b4d6d92772bd8cb75c3fc20`  
		Last Modified: Mon, 03 Apr 2023 21:15:23 GMT  
		Size: 4.8 MB (4830709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b035d251fafecd9ff4a4ebffcae28d4407c686c7620b5a8620e10d3a9bef189e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18073372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344f2374f3e3534bcd7d00b2614a5c285fb3ac1f2a650f452ec39db1574f6dca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:43:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 15 Jun 2023 00:43:52 GMT
ENV HOME=/home/user
# Thu, 15 Jun 2023 00:43:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 15 Jun 2023 00:43:53 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 00:43:53 GMT
ENV IRSSI_VERSION=1.4.4
# Thu, 15 Jun 2023 00:44:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Thu, 15 Jun 2023 00:44:05 GMT
WORKDIR /home/user
# Thu, 15 Jun 2023 00:44:05 GMT
USER user
# Thu, 15 Jun 2023 00:44:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c54f3183a6aa1b85d778dda839e45ee8ad6a0f52b1779f546a66b4164d3d30`  
		Last Modified: Thu, 15 Jun 2023 00:44:21 GMT  
		Size: 9.7 MB (9747425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc912d53522d5fd879d9ec51550b99b23c7ecb7b97fe6a787f67438ea3a0b5`  
		Last Modified: Thu, 15 Jun 2023 00:44:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87e8eea308f83f089095f91e5e10dbf9a2be0b6655af2d8e0c35e1b1b39bc3`  
		Last Modified: Thu, 15 Jun 2023 00:44:20 GMT  
		Size: 5.1 MB (5063526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:67af0601d95928bf581e7ea3707156464ead75575cda6db3d4f745bbbb90dfd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17776210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeece3c8d89e05b389913f16f910701c50ae07e4cfd6346b86eee3ba398315f`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 20:39:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 03 Apr 2023 20:39:20 GMT
ENV HOME=/home/user
# Mon, 03 Apr 2023 20:39:21 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 03 Apr 2023 20:39:21 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 20:39:21 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 03 Apr 2023 20:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 03 Apr 2023 20:39:52 GMT
WORKDIR /home/user
# Mon, 03 Apr 2023 20:39:52 GMT
USER user
# Mon, 03 Apr 2023 20:39:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e6697fdaca36de7d94fb144034d14e7031d715a67abe6c6576bb3b304981ef`  
		Last Modified: Mon, 03 Apr 2023 20:40:19 GMT  
		Size: 9.1 MB (9111252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d6e700458e83183512ad004bc37fa7c64e57d78bc3423667b56a317e491b7e`  
		Last Modified: Mon, 03 Apr 2023 20:40:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940a4d865d72daa94ce432ab539ccc398e48b33797ae51bc0d8b1eea65f16866`  
		Last Modified: Mon, 03 Apr 2023 20:40:17 GMT  
		Size: 5.3 MB (5251413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:edbac3bc69ae83f6a98c2aad44f19c80a109631cb22bd3fa7f0c500242c62faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18484325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94c29de632503a0823c113d66340f5bc25c0af8ef7e8bff75880144aa1c2f0`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:12:08 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 15 Jun 2023 02:12:09 GMT
ENV HOME=/home/user
# Thu, 15 Jun 2023 02:12:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 15 Jun 2023 02:12:10 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 02:12:11 GMT
ENV IRSSI_VERSION=1.4.4
# Thu, 15 Jun 2023 02:12:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Thu, 15 Jun 2023 02:12:35 GMT
WORKDIR /home/user
# Thu, 15 Jun 2023 02:12:35 GMT
USER user
# Thu, 15 Jun 2023 02:12:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864111a1d0261ae544596480b7c499eeaf06cbbe1bc28790c10c4f7c970266cc`  
		Last Modified: Thu, 15 Jun 2023 02:12:54 GMT  
		Size: 9.8 MB (9819563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0ad87a302112668f0b2d1aa81c90fea805716562d224e498f265e8fbc40ed9`  
		Last Modified: Thu, 15 Jun 2023 02:12:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc50b4b50b6a0ce01de8d1e1e0c6e619054efd5e6110152ccb85f0d07e940776`  
		Last Modified: Thu, 15 Jun 2023 02:12:52 GMT  
		Size: 5.3 MB (5273573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:024d71e5b780677e8435851d8d29905d045ebe07c06921ce2f6848ff318a8fc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20380452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3206dacacf5a2e91878b1c1305ffd2b7185860015035893aea8b5a2d562836a7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Wed, 03 May 2023 12:20:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 03 May 2023 12:20:36 GMT
ENV HOME=/home/user
# Wed, 03 May 2023 12:20:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 03 May 2023 12:20:37 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 12:20:37 GMT
ENV IRSSI_VERSION=1.4.4
# Wed, 03 May 2023 12:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 03 May 2023 12:21:07 GMT
WORKDIR /home/user
# Wed, 03 May 2023 12:21:08 GMT
USER user
# Wed, 03 May 2023 12:21:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321e3ba92b8c4c35e093a264c0cd71242bc2328ef4d0e07099549a20c6f758aa`  
		Last Modified: Wed, 03 May 2023 12:21:42 GMT  
		Size: 10.2 MB (10161269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cf72de3a1c69a2ed65ef8a3de45b1d228b2ab27b51684144827d2c2d180ca0`  
		Last Modified: Wed, 03 May 2023 12:21:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05f1871c61a2a542a7dde306681e2c5a63ff71e394a4915337f3e00cee0b61`  
		Last Modified: Wed, 03 May 2023 12:21:41 GMT  
		Size: 7.0 MB (7042712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
