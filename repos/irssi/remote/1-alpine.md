## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:d155b42dcddee4507e1509415c973230d9c558eead034b53e78bd1ce5bd9bb73
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

### `irssi:1-alpine` - linux; amd64

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

### `irssi:1-alpine` - linux; arm variant v6

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

### `irssi:1-alpine` - linux; arm variant v7

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

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9c1674322a4a859b313630ab63bc5068c74372d76d2cdcdd037001859aad99aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18073319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68075a8da11313fe9ff84c7032ac7eb847db620d923f099dda69b33c6809a4fd`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 20:50:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 03 Apr 2023 20:50:33 GMT
ENV HOME=/home/user
# Mon, 03 Apr 2023 20:50:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 03 Apr 2023 20:50:33 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 20:50:33 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 03 Apr 2023 20:50:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 03 Apr 2023 20:50:47 GMT
WORKDIR /home/user
# Mon, 03 Apr 2023 20:50:47 GMT
USER user
# Mon, 03 Apr 2023 20:50:47 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83262423e49eb144f458e46528582b33f5e4a85f7d2ee72a9765a523c0742af8`  
		Last Modified: Mon, 03 Apr 2023 20:51:11 GMT  
		Size: 9.7 MB (9746835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c836451850e08c0bb96fbfbb49284de22329f72ec994ae1a1cb4c7cee00850`  
		Last Modified: Mon, 03 Apr 2023 20:51:10 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b038fab9cea41ad5f562660318726e85d859711cb3776d18e6f4ed903389d8`  
		Last Modified: Mon, 03 Apr 2023 20:51:10 GMT  
		Size: 5.1 MB (5063349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; 386

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

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:430a8c77e55cc72638b0d054d7495a64a27525b452c34c877f6c8836fdc682dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18485815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd96ed4a93def0afd3233164bed8bd5222cf83a26f8921ffb5404ca39431a2c7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:27 GMT
ADD file:e95c1f256ba4bda85c5cbc0d8e84e6f329aa17c9dd2715b2da043e2139049124 in / 
# Wed, 29 Mar 2023 18:16:28 GMT
CMD ["/bin/sh"]
# Mon, 03 Apr 2023 21:36:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 03 Apr 2023 21:36:34 GMT
ENV HOME=/home/user
# Mon, 03 Apr 2023 21:36:36 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 03 Apr 2023 21:36:36 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 21:36:37 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 03 Apr 2023 21:37:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 03 Apr 2023 21:37:12 GMT
WORKDIR /home/user
# Mon, 03 Apr 2023 21:37:13 GMT
USER user
# Mon, 03 Apr 2023 21:37:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1b7d25764eb3d3c55d73f5dfb9e3e9d75f3f39132e1b16142319de2a062dd673`  
		Last Modified: Wed, 29 Mar 2023 18:17:14 GMT  
		Size: 3.4 MB (3390935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20eeec110a634f21fa855f6a0f3bb4bf0cbf9a9c829bce6174c255a7cbff7838`  
		Last Modified: Mon, 03 Apr 2023 21:37:47 GMT  
		Size: 9.8 MB (9820162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0669d6ddb17ff65e87bb10d98d574c6b43455c9453d68ed39daff4369563f36`  
		Last Modified: Mon, 03 Apr 2023 21:37:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dccd5e58c60b670b0951a6c8f01996d28642ecf69691a813760ca329ea259a`  
		Last Modified: Mon, 03 Apr 2023 21:37:45 GMT  
		Size: 5.3 MB (5273434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; s390x

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
